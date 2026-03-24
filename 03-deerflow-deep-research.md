# Case Study 03: DeerFlow for Chapter-Level Deep Research

**Author:** Lee Yongwook, Professor of Korean Language and Literature, Jeonju University  
**Stack:** DeerFlow · LangGraph · nginx · WSL2/Ubuntu  
**Use case:** Book-level research synthesis (14 chapters)  
**Date:** March 2026

---

## Overview

DeerFlow is an open-source deep research agent (ByteDance) built on LangGraph. Unlike single-prompt AI tools, it runs an autonomous research loop: form question → search → synthesize → identify gaps → repeat. Output is a structured research report (3,000–6,000 words for chapter-level queries).

**Role in the pipeline:**
```
DeerFlow (external literature synthesis)
    → 성준/RAG (cross-reference own corpus)
    → Claude (argument design + drafting)
    → Human (judgment, integration, voice)
```

---

## System Architecture

```
PC2 (Lenovo Legion, WSL2/Ubuntu)
├── DeerFlow server (port 2026)
│   ├── LangGraph backend
│   └── Next.js frontend
├── nginx (reverse proxy, port 2026)
└── WSL2 (Ubuntu, username: leeyongwook)
    └── hostname: DESKTOP-GA4FNS2
        external IP: 202.31.234.137
```

**Startup sequence:**
```bash
# After reboot - manual fallback if scheduled tasks fail
~/start-research.sh          # in WSL
C:\wsl-autostart.ps1         # in admin PowerShell
```

**Scheduled tasks (Windows):**
- `WSL-AutoBoot` — starts WSL on system boot
- `WSL-SSH-AutoStart` — starts SSH service in WSL

---

## Installation

### Prerequisites

```bash
# WSL2/Ubuntu
sudo apt update && sudo apt install -y nodejs npm python3 python3-pip

# Clone DeerFlow
git clone https://github.com/bytedance/deerflow.git
cd deerflow
npm install
pip install -r requirements.txt
```

### Configuration

**`.env.local` (critical — browser routing through nginx):**
```env
NEXT_PUBLIC_API_URL=http://localhost:2026
LANGGRAPH_API_URL=http://0.0.0.0:2026
LANGGRAPH_MAX_WORKERS=10
```

**nginx configuration (`/etc/nginx/sites-available/deerflow`):**
```nginx
server {
    listen 2026;
    
    location /api/ {
        proxy_pass http://localhost:8123/;
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection 'upgrade';
    }
    
    location / {
        proxy_pass http://localhost:3000/;
    }
}
```

```bash
sudo ln -s /etc/nginx/sites-available/deerflow /etc/nginx/sites-enabled/
sudo nginx -t && sudo systemctl restart nginx
```

### LangGraph Server

```bash
cd deerflow
langgraph up --host 0.0.0.0 --port 8123
```

### Next.js Frontend

```bash
cd deerflow
npm run dev -- --port 3000
```

### Startup Script (`~/start-research.sh`)

```bash
#!/bin/bash
# Start all research infrastructure

# Start Qdrant (if not running)
docker start qdrant 2>/dev/null || echo "Qdrant already running"

# Start Khoj
nohup khoj --host 0.0.0.0 --port 42110 > ~/logs/khoj.log 2>&1 &

# Start DeerFlow LangGraph backend
cd ~/deerflow
nohup langgraph up --host 0.0.0.0 --port 8123 > ~/logs/langgraph.log 2>&1 &

# Start DeerFlow frontend
nohup npm run dev -- --port 3000 > ~/logs/deerflow-frontend.log 2>&1 &

# Start nginx
sudo systemctl start nginx

echo "Research infrastructure started"
echo "DeerFlow: http://localhost:2026"
echo "Khoj: http://localhost:42110"
```

---

## Troubleshooting: Issues Encountered and Fixes

### 1. LangGraph not accessible from browser

**Symptom:** Frontend loads but API calls fail  
**Cause:** LangGraph bound to `localhost` only  
**Fix:**
```bash
# Wrong
langgraph up --port 8123

# Correct
langgraph up --host 0.0.0.0 --port 8123
```

### 2. Stuck worker queues

**Symptom:** Research tasks hang indefinitely, no output  
**Cause:** Worker queue deadlock  
**Fix:** Set in `.env.local`:
```
LANGGRAPH_MAX_WORKERS=10
```
Then restart LangGraph server.

### 3. SSR/CSR hydration error

**Symptom:** `chat-box.tsx` throws hydration mismatch error  
**Fix:** Add to top of `chat-box.tsx`:
```typescript
"use client"
```

### 4. Browser requests not routing correctly

**Symptom:** Frontend shows but API endpoints return 404  
**Cause:** `.env.local` misconfigured  
**Fix:** Ensure `.env.local` points browser requests through nginx:
```env
NEXT_PUBLIC_API_URL=http://localhost:2026
```
Not directly to LangGraph port.

---

## Usage: Chapter Research Workflow

### Research Brief Format

Do not submit bare questions. Frame the research task:

```
Research task: [Clear statement of what needs to be synthesized]

Scope:
- [Subtopic 1]
- [Subtopic 2]  
- [Subtopic 3]

Key questions:
- [Specific question 1]
- [Specific question 2]

Theoretical context: [Your framework — helps DeerFlow 
prioritize relevant sources]

Flag if found: [Specific connections you are looking for]
```

### Example: Dialogicity Research Brief

```
Research task: Survey the concept of dialogicity as it appears 
in (1) Bakhtin's original formulation, (2) subsequent 
applications in media and communication theory, (3) recent 
literature on human-AI interaction.

Key questions:
- How has dialogicity been extended beyond literary contexts?
- What are the main critiques of applying dialogicity to 
  non-human interlocutors?
- Where does the human-AI dialogicity literature currently 
  stand, and what remains undertheorized?

Theoretical context: Artificial Nature Theory — interested in 
dialogicity as the mechanism through which human-AGI 
co-evolution produces knowledge. Connection to Bakhtin's 
self-other relation is central.

Flag if found: Any sources that directly address non-human 
or machine interlocutors within a Bakhtinian framework.
```

### Typical Output Structure

```markdown
# [Topic] — Research Synthesis

## Overview
[2–3 paragraph executive summary]

## Section 1: [Subtopic]
[Detailed synthesis with citations]

## Section 2: [Subtopic]
[...]

## Key Debates
[Map of main positions and fault lines]

## Gaps in Current Literature
[What remains undertheorized]

## Sources
[Bibliography of consulted sources]
```

---

## Integration with RAG System

After DeerFlow produces external synthesis, cross-reference against personal corpus:

```python
# Conceptual flow (not literal code)

deerflow_output = run_deep_research(research_brief)
key_concepts = extract_concepts(deerflow_output)

for concept in key_concepts:
    personal_passages = query_rag(
        agent="성준",
        query=f"What have I written about {concept}?",
        qdrant_url="http://192.168.0.4:6333"
    )
    connections = synthesize_connections(
        external=deerflow_output,
        internal=personal_passages
    )
```

**Key questions for cross-referencing:**
- Where does external literature connect to my prior work?
- Have I already argued this? More or less strongly?
- What did I argue that the external literature has not addressed?
- Where do I contradict myself between 2009 and 2024? (Forces explicit reckoning)

---

## Performance

| Metric | Value |
|--------|-------|
| Typical query time | 15–25 minutes |
| Output length | 3,000–6,000 words |
| Sources consulted per session | 20–40 |
| Chapters in current book | 14 |
| Full corpus synthesis (all chapters) | ~1 week of DeerFlow sessions |

---

## Use in Book Project

**Current project:** 《기술생성시대의 매체미학》  
*(Media Aesthetics in the Age of Technological Generation)*

14 chapters across 5 parts. DeerFlow has been used for:

- Part I: AGI and superintelligence discourse (3 chapters)
- Part II: Dialogicity and human-AGI interaction (3 chapters)  
- Part III: Tool Competency framework (2 chapters)
- Part IV: Metabourgeoisie and future community (3 chapters)
- Part V: Media aesthetics in the Age of Technological Generation (3 chapters)

Each chapter: one DeerFlow session (external synthesis) + one RAG session (internal cross-reference) + Claude drafting + human revision.

---

## Limitations

- **Korean-language sources:** Significantly underperforms on Korean scholarship. Requires manual supplementation for Korean-language literature.
- **Verification required:** DeerFlow sometimes miscites or gets details wrong. Every significant claim needs primary source verification.
- **No close reading:** Synthesizes at the level of arguments and positions, not specific passages. Close reading remains manual.
- **WSL2 stability:** After Windows reboots, requires manual startup sequence. Scheduled tasks handle most cases but not all.
- **Resource intensive:** Deep research sessions consume significant CPU/RAM. Not suitable for running simultaneously with other heavy tasks on PC2.

---

## Files in This Repository

```
deerflow-config/
├── startup-script.sh         — Full infrastructure startup
├── nginx-config.md           — nginx reverse proxy setup
├── env-template.md           — .env.local configuration guide
├── research-brief-template.md — Structured query format
└── troubleshooting.md        — Common issues and fixes
```

*(Guides in progress — will be added as they stabilize)*

---

## Resources

- [DeerFlow GitHub](https://github.com/bytedance/deerflow)
- [LangGraph documentation](https://langchain-ai.github.io/langgraph/)
- Substack essay (conceptual context): [artificialnature.substack.com](https://artificialnature.substack.com)

---

*Part of the Humanities AI Research Infrastructure case study series.*  
*Previous: [Case Study 02 — RAG with Qdrant + Khoj](02-rag-qdrant-khoj.md)*  
*Next: Case Study 04 — OpenSandbox: The Full Orchestration Pipeline*
