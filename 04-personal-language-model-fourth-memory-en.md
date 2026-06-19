# Case Study 04: PLM as Fourth Memory for Humanistic Reading

**Author:** Lee Yongwook, Professor of Korean Language and Literature, Jeonju University
**Stack:** Personal Language Model · RAG · Long-term Memory · Humanistic Reading Logs
**Use case:** Turning accumulated reading traces into a reflective memory system
**Date:** June 2026

---

## Overview

This document presents a practical framework for designing a Personal Language Model (PLM) as **Fourth Memory (M4)**. A PLM is not understood here as a conversational tool that merely remembers prior prompts. It is a structured memory environment that receives a scholar's reading traces, returns them in transformed form, and supports a new relation between human interpretation and machine memory.

The central question is:

> When a scholar's reading notes, annotations, questions, and conceptual revisions accumulate in a language model, do they remain stored data, or can they form a new memory relation between human and non-human agents?

The working claim is that a PLM becomes M4 only when it moves beyond storage and retrieval. It must sustain a recursive cycle of **inscription, resonance, and consonance**.

---

## Conceptual Position

M4 extends, but does not simply repeat, the distinction among biological, cultural, and digital memory.

| Layer | Definition | Main agent | Operation |
|---|---|---|---|
| M1 | Biological memory | Human body and perception | Association, forgetting, reconstruction |
| M2 | Cultural memory | Human communities | Transmission, interpretation, canon formation |
| M3 | Digital memory | Database and algorithmic systems | Storage, search, computation |
| M4 | Consonant memory | Human-nonhuman resonance | Inscription, resonance, consonance |

M4 presupposes M3, but it is not a larger M3. A database can store reading notes; a vector database can retrieve them semantically; a long-context model can summarize them. None of these operations is sufficient by itself. M4 begins when stored traces are returned to the reader in a way that changes the reader's self-understanding.

This places M4 within media aesthetics in the Age of Technological Generation. Memory is no longer only preserved or edited. It becomes generative through interaction.

---

## Why Humanistic Reading Matters

The most suitable input for a PLM-M4 system is not generic activity data. It is humanistic reading.

Humanistic reading produces dense memory traces because it contains at least three layers:

| Layer | Example | Why it matters for PLM |
|---|---|---|
| Text memory | Quotation, summary, bibliographic note | Provides explicit reference material |
| Response memory | Agreement, resistance, question, marginal note | Records interpretive movement |
| Self memory | Changes in the reader's own conceptual position | Gives the system a history of self-revision |

The third layer cannot be fully captured by a model. Tacit knowledge, embodied feeling, and unspoken hesitation remain partly outside the system. This is not a failure of M4. It is the reason M4 must be understood as a relation, not as a complete upload of the self.

---

## PLM Implementation Options

A practical PLM for M4 can combine three technical patterns.

| Pattern | Mechanism | Relation to M4 | Strength | Risk |
|---|---|---|---|---|
| Fine-tuning | Re-train or adapt a model on personal data | Deep inscription | Strong stylistic and conceptual adaptation | Hard to update; echo risk |
| RAG | Store notes in a vector database and retrieve them dynamically | Resonance | Easy to update and inspect | Retrieval quality limits output |
| Long-term memory | Maintain persistent interaction history | Consonance | Supports continuity across sessions | Requires careful governance |

For most humanities workflows, the safest first implementation is a hybrid of RAG and long-term memory:

```text
Reading note / annotation / draft
    -> normalize metadata
    -> chunk by concept and source
    -> embed into vector store
    -> retrieve in response to research questions
    -> return passages with reflective prompts
    -> record the scholar's acceptance, rejection, or revision
```

Fine-tuning should be considered only after the memory corpus is stable and privacy boundaries are clear.

---

## M4 Cycle

The PLM becomes M4 through three repeated moments.

### 1. Inscription

The reader leaves traces such as quotation, summary, question, objection, connection to previous work, and changes in concept definition. These traces are not neutral data. They are interpretive marks made by a situated reader.

### 2. Resonance

The PLM returns the traces in transformed form:

- "This current argument resembles your earlier discussion of Artificial Nature."
- "Your use of memory here shifts from storage to resonance."
- "This note conflicts with your previous distinction between M3 and M4."

Resonance is not agreement. A useful PLM should sometimes disturb the reader's current interpretation.

### 3. Consonance

Over time, the reader and the PLM form a shared memory space. This space is not reducible to the human reader alone or to the machine system alone. It becomes a memory dimension of **WE**, the co-resonant subject formed through human-nonhuman interaction.

---

## Recursive Model

The core process can be expressed as:

```text
M4(t + dt) = M4(t) + alpha * R(t) * Phi[PLM(M4(t))]
```

| Symbol | Meaning |
|---|---|
| `R(t)` | Strength and quality of the reading experience at time `t` |
| `Phi[PLM(M4(t))]` | Resonance function returned by the PLM from the current M4 state |
| `alpha` | Degree of critical acceptance by the reader |

This formula is not an engineering metric ready for direct measurement. It is a design guide. It tells the system designer to track not only what was stored, but also how the reader responded to the system's return.

---

## Healthy and Pathological States

An M4-oriented PLM should distinguish three states.

| State | Condition | Interpretation | Design response |
|---|---|---|---|
| Storage state | `Phi` is close to zero | The PLM behaves like M3 storage | Improve retrieval and reflective prompts |
| Echo state | `alpha` is too high and `Phi` repeats the user | The PLM amplifies existing preferences | Add contradiction search and source diversity |
| Resonant state | `0 < alpha < 1` and `Phi` creates new links | The PLM supports self-revision | Preserve feedback and update memory metadata |

The goal is not perfect personalization. Perfect personalization can become self-imprisonment. The goal is critical resonance.

---

## Suggested Data Schema

A minimal reading-memory record can use the following fields.

```yaml
id: 2026-06-18-m4-plm-note-001
source:
  title: "Book or article title"
  author: "Author name"
  year: 2026
  location: "page, chapter, or URL"
reading_trace:
  quote: "Short quotation or paraphrase"
  summary: "What the passage says"
  response: "Reader's agreement, resistance, or question"
  concept_links:
    - M4
    - PLM
    - Artificial Nature
    - WE
memory_layer: "text | response | self"
plm_return:
  resonance: "How the system returned this trace later"
  reader_alpha: 0.6
  revision: "How the reader changed the argument after the return"
privacy:
  sensitivity: "low | medium | high"
  export_allowed: false
```

The important field is not only `quote` or `summary`, but `revision`. M4 depends on how memory returns and changes the reader.

---

## Workflow for a Humanities PLM

```text
1. Capture reading traces
   - annotations
   - marginal questions
   - conceptual revisions
   - draft fragments

2. Classify memory layer
   - text memory
   - response memory
   - self memory

3. Store in inspectable infrastructure
   - local Markdown
   - vector database
   - versioned metadata

4. Retrieve through research questions
   - concept genealogy
   - contradiction search
   - draft support
   - reviewer objection simulation

5. Return as resonance
   - not only "relevant notes"
   - but tensions, shifts, and forgotten commitments

6. Record reader response
   - accepted
   - rejected
   - revised
   - deferred
```

This workflow keeps the human scholar inside the loop as an interpreter, not merely as a data source.

---

## Governance Principles

Because PLM memory can contain a scholar's deepest interpretive traces, M4 has a political-economic dimension. A PLM can expand self-understanding, but it can also become a mechanism of data capture.

| Principle | Practical rule |
|---|---|
| Local-first memory | Keep canonical notes in user-owned files before platform upload |
| Inspectable retrieval | Store source IDs and passages with every PLM answer |
| Exportability | Avoid memory formats that cannot be moved across systems |
| Critical alpha | Train the user to accept, reject, and revise PLM outputs |
| Anti-echo design | Include contradiction search and counter-memory prompts |
| Sensitive-layer separation | Keep self-memory traces under stricter privacy control |

The political risk is not only surveillance. It is the colonization of self-interpretation. A PLM should help the reader encounter their own memory again, not lock that memory into a platform's profile.

---

## Minimal Prototype

A first prototype does not require model fine-tuning.

```text
Local Markdown archive
    -> metadata parser
    -> embedding pipeline
    -> Qdrant or other vector store
    -> retrieval API
    -> LLM response layer
    -> feedback logger for alpha and revision
```

Prototype tasks:

1. Ingest 50 reading notes with source metadata.
2. Ask the system for concept genealogy across the notes.
3. Ask for contradictions between early and recent definitions.
4. Ask for one resonant return: a passage that changes the current argument.
5. Record whether the reader accepts, rejects, or revises the return.

The test of success is not whether the system produces a fluent summary. The test is whether it helps the scholar recognize a forgotten pattern, tension, or possibility in their own reading history.

---

## Conclusion

A Personal Language Model becomes Fourth Memory only when it is designed as a reflective relation. RAG, fine-tuning, and long-term memory are technical components, but M4 is not reducible to any of them. M4 appears when humanistic reading traces are returned to the reader as resonance and when that return changes the reader's future interpretation.

For humanities research, this reframes AI infrastructure. The central task is not to automate reading, but to build memory environments in which interpretation can return, resist, and transform.

---

## References and Source Notes

- Lee Yongwook. "M4-PLM Integrated Research Report: Fourth Memory, Personal Language Model, and the Ontology of Memory in the Age of Generation." Internal research report, June 18, 2026.
- Bernard Stiegler. *Technics and Time, 1: The Fault of Epimetheus*. Stanford University Press, 1998.
- Michael Polanyi. *The Tacit Dimension*. University of Chicago Press, 1966.
- Paul Ricoeur. *Time and Narrative*. University of Chicago Press, 1984-1988.
- N. Katherine Hayles. *Unthought: The Power of the Cognitive Nonconscious*. University of Chicago Press, 2017.
