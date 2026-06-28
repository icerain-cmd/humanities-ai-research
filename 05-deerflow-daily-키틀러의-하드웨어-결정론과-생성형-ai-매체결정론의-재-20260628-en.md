# Daily DeerFlow Analysis: June 28, 2026

> Is Kittler's hardware determinism still valid in the media environment of the generative AI era? — How should the claim that "media determine our situation" be reconstructed when output is determined by software-level conditions such as model weights, data distributions, and prompt embeddings?

## Question

Is Kittler's hardware determinism still valid in the media environment of the generative AI era? — How should the claim that "media determine our situation" be reconstructed when output is determined by software-level conditions such as model weights, data distributions, and prompt embeddings?

## Key Findings

# Kittler's Hardware Determinism and Generative AI: Toward a Reconstruction of Media Determinism

## 1. The Skeleton of Kittler's Media Determinism

Kittler's media theory consists of three layers:

**(a) The Technological A Priori Thesis** — The opening sentence of "Gramophone, Film, Typewriter" declares: *"Media determine our situation."* Media precede human consciousness and social context as a technological a priori; humans can only think and perceive within the conditions set by media.

**(b) Hardware Reductionism** — In "There Is No Software" (1992), Kittler argues that software is nothing but a marketing abstraction that conceals the material conditions of hardware. All high-level programming languages, operating systems, and UIs can ultimately be reduced to CPU machine instructions and gate-level electrical switching. **Peel away the veneer of software, and the materiality of hardware (silicon, wiring, transistors) always reveals itself.**

**(c) Sequential Media Differentiation** — For Kittler, media are apparatuses that technically segment and fix human sensory channels (hearing, sight, writing). The gramophone captures the auditory data stream, film captures the visual data stream, and the typewriter captures the written data stream — each in a medium-specific way. Each medium determines **the range of what can be stored, processed, and transmitted** through its unique hardware architecture.

---

## 2. The Fundamental Challenge Posed by Generative AI

The media environment of generative AI (LLMs, Vision Models) shakes Kittler's deterministic framework at three points.

### 2.1. The Paradox of a "Softwareless World": A Statistical Layer Irreducible to Machine Code

The core of Kittler's argument in "There Is No Software" is that *"everything ultimately converges to voltage differences (0s and 1s)."* However, LLM operation involves the following layers:

| Layer | Kittlerian Reducibility | Reality |
|-------|-------------------------|---------|
| **Hardware** (GPU, TPU) | O — physical semiconductors | Exists but not deterministic |
| **Machine Code/Assembly** | O — ultimate reductive base | Yet operations themselves are standardized |
| **Model Weights** | △ — floating-point arrays in memory | **Encodes statistical distributions of meaning** |
| **Data Distribution** | X — compressed into weights but irreducible | **Statistical regularities of training data** |
| **Latent Space** | X — no physical location | **Topological semantic space** |
| **Prompt Embeddings** | X — contextual transformation of user input | **Creates different semantic vectors each time** |

For Kittler, software was an 'illusion' of hardware. But generative AI's **model weights** form not mere machine instructions but a **third ontological layer** — statistical correlations extracted from trillions of texts. This layer executes atop physical transistors, yet its content (the distribution of meaning) is not reducible to the physicality of transistors.

Here, Kittler's original thesis is precisely inverted: the counter-thesis — **"Only software exists, and hardware is merely its physical substrate (Substrat)"** — becomes plausible.

### 2.2. Two Types of Determinism: Hardware Determinism vs. Statistical Determinism

Kittler's determinism has the following structure:

```
Hardware architecture → Determines processable data types → Determines conditions of perception/cognition
```

This is **categorical determinism**: it sets the a priori scope of what kinds of information can be stored and processed.

However, the medium of LLMs performs a different kind of determination:

```
Training data distribution + Model architecture (SHA) → 
Statistical structure of weight space → 
Probabilistic output distribution (token prediction)
```

This is **statistical determinism**: it determines not which individual output will appear, but **the probability distribution of outputs**. The experimental fact that the same prompt can produce different outputs even at Temperature = 0 proves that this statistical determinism is qualitatively different from Kittler's hardware determinism.

### 2.3. Prompt Engineering: The Emergence of Immaterial 'Media-Operation'

In Kittler's system, media are controlled through the manipulation of physical devices (typewriter key presses, gramophone needle replacement). But prompt engineering:

- **Manipulates no physical hardware whatsoever** (same GPU, same model weights)
- **Through purely semantic-level input changes**
- **Produces dramatically different output results**

This is a new form of media-operation that Kittler never anticipated. Prompt embeddings are a transformation **within a purely semantic vector space** that determines media output independently of the physical state of hardware.

---

## 3. Direction of Reconstruction: Three-Layer Media Determinism

To reconstruct Kittler's hardware determinism for the generative AI era, I propose the following **three-layer determinism**:

```
[Layer 3: Statistical Determination Layer]
Training data distribution → Weight manifold → Output probability distribution
    ↕ (upward constraint)
[Layer 2: Algorithmic Determination Layer]  
GPU architecture (CUDA cores, memory bandwidth) → 
Scope of computable model size/complexity
    ↕ (upward constraint)
[Layer 1: Physical Determination Layer] ← Kittler's classical domain
Semiconductor physics (transistor switching, thermodynamic limits) → 
Physical foundation of information processing
```

**The core thesis of reconstruction** is as follows:

> Kittler's thesis remains **valid at Layer 1 (physical determination layer)** . All LLM operations ultimately execute on GPU transistor switching. However, Layer 1 is a **necessary condition**, not a **sufficient condition**. What determines the specific output of LLM media is the operation of Layer 3 (statistical determination layer), where the topological structure of weight space, data distribution bias, and contextual transformation of prompt embeddings exercise a more powerful determinative force than hardware.

---

## 4. Conclusion: The Dialectical Transformation of "Media Determine Our Situation"

Kittler's original proposition — *"Media determine our situation"* — must be transformed in the generative AI era as follows:

| Kittler (1980s-90s) | Reconstruction (2020s) |
|---------------------|----------------------|
| Media = hardware apparatuses | Media = **stacked structure** of hardware + software + statistical distribution |
| Determination = a priori conditioning by hardware | Determination = probabilistic conditioning by **statistical ensemble** |
| Human = effect of media | Human (prompt) = **co-determinant** of media output |
| Software = illusion | Software (weights, embeddings) = **new materiality** |

Kittler's hardware determinism is **insufficient on its own** in the media environment of generative AI. But this does not mean it should be discarded. On the contrary, Kittler's materialist insight — that media possess **their own inherent operational logic** independent of human intention — becomes even more important in the generative AI era.

The difference is that this 'inherent operational logic' is no longer the physicality of transistors, but the **topological structure of weight space** and the **statistical bias of data distributions**. Kittler's framework must therefore be expanded into a **statistical media theory**. That is, the proposition **"media determine our situation"** remains intact, but the definition of 'media' must be reconceptualized as a **triple-stacked entity of hardware-algorithm-data** — this is the final conclusion of this analysis.

## Reference
- DeerFlow: June 28, 2026 21:00 KST | Model: DeepSeek V4 Flash
- Full analysis: /mnt/d/paper_md/생성논문/20260628210530_기술생성시대의 매체미학_1문항.md