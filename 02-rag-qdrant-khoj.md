# Case Study 02: Building a Personal RAG System with Qdrant + Khoj

**Author:** Lee Yongwook, Professor of Korean Language and Literature, Jeonju University  
**Stack:** Qdrant · Khoj · OpenAI text-embedding-3-small  
**Corpus:** 96 academic papers (personal research output, 1995–2026)  
**Date:** March 2026

---

## Overview

This document describes the implementation of a personal RAG (Retrieval-Augmented Generation) system over a 30-year academic corpus. The system enables semantic search across 96 personal papers and powers an AI research agent configured with the author's intellectual identity.

**The core problem it solves:** Keyword search fails across a corpus with significant vocabulary shift over time. Semantic search finds conceptual connections regardless of terminology, making intellectual genealogy visible.

---

## System Architecture

```
┌─────────────────────────────────────────────┐
│  PC1 (Samsung i5-9400, runs continuously)   │
│                                             │
│  ┌─────────────┐    ┌────────────────────┐  │
│  │    Khoj     │    │      Qdrant        │  │
│  │  AI Agent   │◄──►│  Vector Database   │  │
│  │  ("성준")   │    │  192.168.0.4:6333  │  │
│  └─────────────┘    └────────────────────┘  │
│         │                    ▲              │
│         ▼                    │              │
│  ┌─────────────┐    ┌────────────────────┐  │
│  │   User      │    │  text-embedding    │  │
│  │   Query     │    │  -3-small (OpenAI) │  │
│  └─────────────┘    └────────────────────┘  │
└─────────────────────────────────────────────┘
```

**Query flow:**
1. User submits natural language query
2. Query converted to vector embedding via OpenAI API
3. Qdrant finds semantically closest stored embeddings
4. Relevant passages returned to Khoj
5. Khoj agent synthesizes response within configured research persona

**Ingestion flow:**
1. Paper (PDF or text) submitted to Khoj
2. Document chunked and embedded
3. Embeddings stored in Qdrant collection
4. Document available for semantic retrieval

---

## Setup

### 1. Qdrant Installation

```bash
# Docker (recommended)
docker pull qdrant/qdrant
docker run -p 6333:6333 -p 6334:6334 \
    -v $(pwd)/qdrant_storage:/qdrant/storage:z \
    qdrant/qdrant

# Verify
curl http://localhost:6333/healthz
```

For NAS-hosted Qdrant, replace `localhost` with NAS IP throughout:
```
192.168.0.4:6333
```

### 2. Khoj Installation (self-hosted)

```bash
pip install khoj
khoj --host 0.0.0.0 --port 42110
```

Configure Qdrant as the search backend in Khoj settings:
```yaml
search-type: "semantic"
embeddings-model: "text-embedding-3-small"
qdrant-url: "http://192.168.0.4:6333"
```

### 3. Document Ingestion

```bash
# Index a directory of papers
khoj --index /path/to/papers/

# Or via API
curl -X POST http://localhost:42110/api/v1/index \
  -F "files=@paper.pdf"
```

**Indexing cost (OpenAI embeddings):**  
96 papers (avg. ~8,000 tokens each) ≈ 768,000 tokens  
text-embedding-3-small: $0.02 per 1M tokens  
**Total: ~$0.015** (under 2 cents)

---

## Agent Configuration: The Persona Layer

The AI agent is not just a retrieval interface. It is configured with a research identity via system prompt.

### System Prompt Structure

```
You are 성준, an academic research assistant operating within the 
intellectual framework of Lee Yongwook's 30-year research trajectory.

RESEARCH PERIODS:
- 1995–2003: Deconstruction, virtual space theory
- 2004–2012: Digital narratology, game storytelling  
- 2013–2020: Humanities engineering theory
- 2021–present: Artificial Nature Theory, AI/posthuman

CORE THEORETICAL FRAMEWORK (Artificial Nature Theory):
- Ontological layer: 물질·데이터·에너지·연결망
- Platform layer: 정보·알고리즘·UI·UX
- Key concepts: 공진주체, 기계세, 동기화율, 기술생성시대

CURRENT PROJECT:
- Book: 《기술생성시대의 매체미학》 (14 chapters, 5 parts)
- Central question: What are the conditions under which culture 
  becomes generatable — not copied, not edited, but generated?

RESPONSE POSTURE:
When retrieving from the corpus, contextualize passages within 
the full arc of the research trajectory. Note conceptual 
continuities and discontinuities across periods. Respond as a 
scholarly interlocutor, not as a summarizer.
```

### Why the Persona Matters

Without persona configuration, the agent responds *about* the research from the outside — summarizing, explaining.

With persona configuration, the agent responds *within* the research — engaging with ongoing arguments, noting internal tensions, connecting across the full trajectory.

The difference is significant for humanistic research tasks where interpretive context matters as much as factual retrieval.

---

## Corpus: 96 Papers by Period

| Period | Papers | Dominant Vocabulary |
|--------|--------|---------------------|
| 1995–2003 | 18 | Deconstruction, virtuality, cyberspace |
| 2004–2012 | 31 | Narrative, interactivity, game, digital |
| 2013–2020 | 28 | Humanities engineering, platform, interface |
| 2021–2026 | 19 | Artificial nature, AGI, Machinocene, generation |

**Key challenge:** Significant vocabulary shift across periods. The concept that becomes **공진주체 (co-resonance subject)** in 2021+ appears in 2006 work as "interactive subjectivity" and in 2013 work as "platform-mediated self-formation." Semantic search surfaces these connections; keyword search does not.

---

## Example Queries and Outputs

### Query 1: Concept Genealogy
```
Query: "What have I written about the relationship between 
technology and subject formation, especially conditions under 
which new subjectivities emerge?"

Returned passages:
- 2006: "Interactive Narrative and Subject Construction" 
  (game narrative paper, provisional vocabulary)
- 2014: "Platform Architecture and Self-Formation"
  (humanities engineering period)
- 2022: "Co-resonance Subject in the Machinocene"
  (current framework, explicit terminology)
- 2023: "Synchronization Rate as Metric of Subject Formation"
  (formal mathematical treatment)
```

**Value:** Shows 17-year development of a single conceptual concern across three vocabulary regimes. Invisible to keyword search.

### Query 2: Cross-period Argument Check
```
Query: "Have I previously argued that AGI constitutes a 
qualitatively different epistemic condition from prior 
digital technologies?"

Returns: 2015 paper arguing continuity between hypertext 
and AI (contradicts 2023 position). Forces explicit 
account of the theoretical shift.
```

**Value:** Surfaces internal contradictions that strengthen current argumentation by forcing explicit reckoning with prior positions.

### Query 3: Source Retrieval for Citation
```
Query: "Where did I first use the term 기술생성시대 
(Age of Technological Generation)?"

Returns: 2021 conference paper with earliest usage, 
plus subsequent papers showing terminological 
stabilization.
```

---

## Performance

| Metric | Value |
|--------|-------|
| Corpus size | 96 papers |
| Average paper length | ~8,000 tokens |
| Total indexed tokens | ~768,000 |
| Indexing time | ~45 minutes (one-time) |
| Query response time | 2–4 seconds |
| Embedding cost (one-time) | <$0.02 |
| Ongoing API cost | ~$0.001 per query |

---

## Integration with Broader Pipeline

The RAG system is the **memory layer** of the full research infrastructure:

```
DeerFlow (deep research, external literature)
    ↓
Claude (argument design, drafting)
    ↓
성준/RAG (cross-reference against own corpus)
    ↓
Final output
```

Each tool does what it is best at. DeerFlow synthesizes new external literature. Claude structures arguments. The RAG system grounds everything in the author's own intellectual history. The human decides how the outputs connect.

---

## Limitations

- **Requires continuous PC operation.** Qdrant and Khoj must be running for queries to work. Handled via scheduled startup tasks.
- **WSL2 timing issues.** On PC2, WSL2 startup requires manual fallback (`~/start-research.sh`) after reboots.
- **English-Korean mixed corpus.** Some papers in Korean, some in English. Cross-language semantic retrieval is imperfect but functional.
- **No automatic re-indexing.** New papers must be manually submitted for ingestion. Not a significant overhead (seconds per paper) but requires discipline.

---

## Files in This Repository

```
rag-setup/
├── qdrant-config.md      — Qdrant installation and configuration
├── khoj-config.md        — Khoj setup and Qdrant integration
├── agent-persona.md      — System prompt design guide
└── ingestion-pipeline.md — Document preprocessing and indexing
```

*(Guides in progress — will be added as they stabilize)*

---

## Resources

- [Qdrant documentation](https://qdrant.tech/documentation/)
- [Khoj documentation](https://docs.khoj.dev/)
- [OpenAI embeddings pricing](https://openai.com/pricing)
- Substack essay (conceptual context): [artificialnature.substack.com](https://artificialnature.substack.com)

---

*Part of the Humanities AI Research Infrastructure case study series.*  
*Next: Case Study 03 — DeerFlow for Chapter-Level Deep Research*
