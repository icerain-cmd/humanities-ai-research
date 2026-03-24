# Case Study 01: Why Humanists Need Local AI Infrastructure

**Author:** Lee Yongwook, Professor of Korean Language and Literature, Jeonju University  
**Research Framework:** Humanities Engineering · Artificial Nature Theory  
**Date:** March 2026

---

## The Problem

Most AI research tools are built by engineers for engineers. The assumptions embedded in their design — what counts as a useful query, what kinds of outputs matter, what the workflow looks like — reflect engineering problems, not humanistic ones.

Humanists work differently. The central operations of humanistic research are:

- **Concept genealogy** — tracing how an idea develops across texts, disciplines, and time
- **Argumentative synthesis** — constructing positions that hold together across heterogeneous sources
- **Interpretive contextualization** — situating claims within cultural, historical, and theoretical fields
- **Long-form coherence** — sustaining a single argument across book-length projects

None of these are well-served by generic AI tools optimized for question-answering or code generation.

The deeper problem is epistemic. If your research is about how technological systems shape the conditions of cultural experience — which mine is — you cannot do that research well while being entirely dependent on opaque systems you cannot inspect, configure, or theorize. The conditions under which thinking happens matter. A humanist who outsources their epistemic infrastructure to black-box products is working in a condition of theoretical inconsistency.

---

## The Solution: Own Your Epistemic Infrastructure

Building your own AI research infrastructure is not primarily a technical project. It is a theoretical commitment made concrete.

The core principle: **the tools through which you think should be legible to you, configurable by you, and aligned with your actual research workflow — not a generic workflow designed for someone else.**

This means:

- Local or self-hosted systems where possible (data stays with you)
- Open-source components you can inspect and modify
- Configuration that reflects your actual research identity
- A stack designed around humanistic operations, not engineering operations

---

## The Stack (as of March 2026)

```
PC1 (Samsung i5-9400)
├── Khoj AI Agent          — Conversational research interface
├── Qdrant Vector DB       — Semantic search over personal corpus
│   └── NAS: 192.168.0.4:6333
└── OpenAI text-embedding-3-small

PC2 (Lenovo Legion, WSL2/Ubuntu)
├── DeerFlow (port 2026)   — Deep research agent (ByteDance open-source)
└── OpenSandbox (port 8501) — 10-menu Streamlit research assistant
    ├── Paper pipeline (R1→R2→R2_elicit→summarize→R3 A/B/C→Part D)
    ├── Artificial Nature Analysis
    ├── Concept Genealogy Tracking
    ├── PDF Analysis
    └── Auto Presentation Generation
```

**LLM routing (cost-conscious):**
- DeepSeek-chat: multi-step pipeline calls
- Claude: argument design and drafting
- Perplexity: external literature search
- Local RAG (성준): cross-referencing own corpus

---

## What This Enables

### 1. Querying Your Own Corpus Semantically

96 papers indexed in Qdrant. Natural language queries return semantically relevant passages across the full corpus — regardless of when they were written or what vocabulary they used.

Example query: *"What have I written about the relationship between technology and subject formation?"*

Returns passages from four papers across three decades, including a 2006 paper on game narrative that uses provisional vocabulary for what later became the **공진주체 (co-resonance subject)** concept. That connection was invisible to keyword search.

### 2. Concept Genealogy Tracking

Trace how a theoretical concept develops across your own work and across secondary literature. The pipeline combines RAG retrieval (own corpus) with DeerFlow deep research (external literature) to produce a synthetic genealogy.

### 3. Multi-Stage Argumentative Pipeline

The orchestrator pipeline moves through stages designed for humanistic argumentation:

```
R1 (literature survey)
→ R2 (core argument construction)
→ R2_elicit (counterargument elicitation)
→ summarize
→ R3 A/B/C (three-branch development)
→ Part D (integration)
```

Each stage has a different epistemic posture. This is not a single-prompt output; it is a structured thinking environment.

### 4. Research Identity Preservation

The AI agent (named 성준) has a system prompt encoding:
- Four periods of 30-year research trajectory
- Core theoretical concepts and their relationships
- Characteristic argumentative moves
- Current book project and its chapter structure

Responses are calibrated to this intellectual framework, not to generic academic discourse.

---

## Key Design Decisions

**Why self-hosted Qdrant rather than a cloud vector DB?**  
Data stays local. For a corpus of personal unpublished research, this matters both practically (no API costs at scale) and principally (your intellectual archive should not live on someone else's server).

**Why Khoj rather than a custom RAG pipeline?**  
Khoj provides the conversational interface and agent persona layer without requiring custom development of the retrieval pipeline. For humanists who are not developers, this significantly lowers the barrier.

**Why separate machines?**  
PC1 runs continuously as the persistent knowledge infrastructure (RAG, vector DB, agent). PC2 handles computationally intensive pipeline tasks (DeerFlow deep research, multi-stage orchestration) on demand. The separation prevents resource contention and allows each machine to be optimized for its role.

**Why not just use ChatGPT?**  
ChatGPT does not have access to your corpus. It cannot cross-reference your own intellectual history. It responds from the outside of your research, summarizing and explaining. A configured local agent responds from the inside, engaging with the ongoing arguments. The difference in output quality for humanistic research tasks is significant.

---

## Theoretical Grounding

This infrastructure is built on a theoretical commitment from **Artificial Nature Theory (인공자연론)**:

Contemporary platforms and AI systems constitute an **artificial nature** — a second nature that is not merely mediated by technology but architecturally organized through it. The eight foundational elements of this artificial nature:

**Ontological layer:** Material · Data · Energy · Network  
**Platform layer:** Information · Algorithm · UI · UX

Platforms are not neutral conduits. They are environments that shape what kinds of thinking are easy, what kinds are hard, what gets surfaced and what gets suppressed. Building your own research infrastructure is an act of reclaiming agency over your epistemic environment.

The humanist who uses only commercial AI products is conducting research inside an environment they did not design and cannot inspect. The humanist who builds their own infrastructure is conducting research inside an environment they have theorized.

---

## Limitations and Honest Assessment

- **Setup time:** Getting Qdrant, Khoj, and DeerFlow working together took significant iterative troubleshooting. Not a weekend project.
- **Maintenance overhead:** WSL2 boot timing issues, port conflicts, scheduled tasks — the infrastructure requires ongoing attention.
- **Not for non-technical users:** The current setup requires comfort with command line, basic networking, and reading error logs. A simpler version using hosted Khoj is possible but less powerful.
- **Embedding costs:** Minimal but not zero. Indexing 96 papers with OpenAI embeddings cost under $1. Ongoing costs are negligible at this scale.

---

## Resources

- Full README: [github.com/icerain-cmd/humanities-ai-research](https://github.com/icerain-cmd/humanities-ai-research)
- Detailed RAG setup: see `rag-setup/` directory
- Substack post (expanded essay version): [artificialnature.substack.com](https://artificialnature.substack.com)

---

*Part of the Humanities AI Research Infrastructure case study series.*
