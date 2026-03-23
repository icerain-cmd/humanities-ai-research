# Humanities AI Research Infrastructure

**A scholar-built stack for humanists who want to own their research environment.**

Built and maintained by [Lee Yongwook](https://github.com/leeyongwook), Professor of Korean Language and Literature, Jeonju University.  
Research field: **Humanities Engineering** — humanistic inquiry that understands, interprets, and leads technology.  
Core interests: **Artificial Nature Ontology** · **Media Aesthetics in the Age of Technological Generation**

---

## What This Is

Most AI research tools are built by engineers for engineers. This repository documents a different kind of infrastructure — one designed from within humanistic inquiry, where the questions are about meaning, genealogy, and theoretical coherence rather than throughput and benchmarks.

The underlying framework is **Artificial Nature Theory (인공자연론)**: a conceptual model in which platforms, algorithms, interfaces, and user experience are not neutral tools but ecological conditions that shape how culture is produced, distributed, and felt. Every component of this stack is built to serve that kind of thinking.

A central concept driving this work is the **Age of Technological Generation (기술생성시대)** — a periodization that moves beyond prior epochs:

| Era | Defining Operation |
|-----|-------------------|
| Age of Technological Copying (기술복사시대) | Reproduction and circulation of existing cultural forms |
| Age of Technological Editing (기술편집시대) | Recombination, curation, and remix as primary cultural logic |
| **Age of Technological Generation (기술생성시대)** | **Generative AI and Artificial Nature as conditions of cultural production itself** |

The Age of Technological Generation is not simply "more powerful tools." It marks a structural shift in which Artificial Nature and AGI become the technical substrate upon which cultural meaning is generated — not reproduced, not edited, but originated at the intersection of human intent and machine generativity. Media aesthetics in this age requires new frameworks. This repository is part of building them.

This is not a tutorial for absolute beginners. It is a working research environment shared openly, with the belief that humanists should control their own epistemic infrastructure.

---

## The Stack

```
PC1 (Samsung i5-9400)
├── Khoj AI Agent ("성준")          — RAG-powered academic persona
├── Qdrant Vector DB               — 96 papers indexed (NAS: 192.168.0.4:6333)
└── OpenAI text-embedding-3-small  — semantic search across own corpus

PC2 (Lenovo Legion, WSL2/Ubuntu)
├── DeerFlow (port 2026)           — deep research agent (ByteDance open-source)
├── OpenSandbox Streamlit UI (port 8501) — 10-menu research assistant
│   ├── 논문 파이프라인 (Paper Pipeline)
│   ├── 인공자연 분석 (Artificial Nature Analysis)
│   ├── 개념 계보 추적 (Concept Genealogy Tracking)
│   ├── 논문 PDF 분석 (PDF Analysis)
│   └── PPT 자동 생성 (Auto Presentation)
└── Orchestrator: R1→R2→R2_elicit→summarize→R3(A/B/C)→Part D
```

**Cost-conscious LLM routing**: DeepSeek-chat (preferred over deepseek-reasoner for multi-step calls), Claude for argument design and drafting, Perplexity for external literature search.

---

## Core Concepts

This stack is built around **Artificial Nature Theory**, which posits that contemporary platforms constitute a second nature — not metaphorically, but structurally. The analytical framework uses eight foundational elements:

**기저 4원소 (Ontological Foundation)**
> Material · Data · Energy · Network

**기층 4원소 (Platform Operating Principles)**
> Information · Algorithm · UI (User Interface) · UX (User Experience)

Platforms are architectural structures built upon the four foundational elements. The research tools in this repository are designed to analyze, trace, and critique how these elements organize cultural experience — particularly in literature, media aesthetics, and the posthuman condition.

Related concepts in active use across this stack:
- **공진주체 (Co-resonance Subject)** — subjectivity formed through platform synchronization
- **기계세 (Machinocene)** — the epoch in which machine agency becomes constitutive of cultural production
- **동기화율 (Synchronization Rate, SR)** — a formal metric: `SR(t) = UX(t) · [I(t)·A(t)] / [1 + μ·UI(t)]`
- **기술편집예술 (Technological Editing Art)** — aesthetic practice native to the Machinocene

---

## Why Open-Source This

Three reasons.

First, humanists should not outsource their epistemic infrastructure to products they cannot inspect or modify. The conditions under which we think matter.

Second, the AI tooling ecosystem for humanities research is nearly empty. There are pipelines for lawyers, doctors, and software engineers. There is almost nothing designed for scholars who work with conceptual genealogy, theoretical argumentation, and long-form interpretive writing.

Third, the work of building this infrastructure has itself become research. Documenting it publicly is part of the inquiry.

---

## Repository Structure

```
/pipelines          — Research orchestration workflows with prompt templates
/rag-setup          — Qdrant + Khoj configuration for academic corpora
/deerflow-config    — DeerFlow tuning for humanities research tasks
/case-studies       — Annotated records of actual research sessions
/theory             — Background on Artificial Nature Theory (English summaries)
/prompts            — Reusable prompt files (copy-paste ready)
```

> ⚠️ This repository is under active construction. Components are documented as they stabilize.

---

## Selected Use Cases

**Concept Genealogy Tracking**
Trace how a theoretical concept (e.g., "the virtual," "the posthuman," "the platform") moves across texts, disciplines, and decades. RAG retrieval surfaces relevant passages; the orchestrator pipeline synthesizes lineage and divergence.

**Paper Pipeline (R1→R3)**
Multi-stage argumentative drafting: literature review (R1) → core argument construction (R2) → elicitation of counterarguments (R2_elicit) → synthesis (summarize) → three-branch development (R3 A/B/C) → integration (Part D).

**Artificial Nature Analysis**
Apply the eight-element framework to any platform, interface, or media artifact. The Streamlit UI walks through each dimension systematically and generates a structured analytical report.

**Synchronization Rate Modeling**
Quantitative formalization of platform-subject relations. Useful for comparative platform analysis and for grounding theoretical claims in measurable terms.

---

## Research Background

30-year trajectory across four periods:

| Period | Focus |
|--------|-------|
| 1995–2003 | Deconstruction, virtual space theory |
| 2004–2012 | Digital narratology, game storytelling |
| 2013–2020 | Humanities engineering theory |
| 2021–present | Artificial Nature Theory, AI/posthuman |

Current book project: **《기술생성시대의 매체미학》** (*Media Aesthetics in the Age of Technological Generation*) — 14 chapters across 5 parts, using the full research stack documented here. The book theorizes media aesthetics at the intersection of Artificial Nature ontology and AGI, where generation — not copying or editing — becomes the fundamental cultural operation.

Affiliated project: **L-HUSS 사업단** (Regional Humanities-Social Sciences consortium), vision: *AIxLocal* — connecting AI research infrastructure to regional cultural value creation.

---

## Following This Work

Weekly notes on research process, infrastructure decisions, and theoretical development:

> **[Artificial Nature — artificialnature.substack.com](https://artificialnature.substack.com)**
> Practical AI workflows for humanists. In Korean and English.

If this work is useful to you, consider supporting it via [GitHub Sponsors — coming soon].

---

## License

Code: MIT  
Writing and theoretical content: CC BY 4.0

---

*"We are no longer in the age of copying culture, nor of editing it. We are in the age of generating it — with machines, through machines, as machines. The question for humanists is not whether to engage this condition, but how to theorize it from within."*
