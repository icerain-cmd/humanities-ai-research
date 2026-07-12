# Daily DeerFlow Analysis: 2026-07-12

> Is Kittler's hardware determinism still valid in the media environment of the generative AI era? — How should the claim that 'the medium determines the message' be reconstructed when output is determined by software conditions such as model weights, data distributions, and prompt embeddings?

## Question

Is Kittler's hardware determinism still valid in the media environment of the generative AI era? — How should the claim that 'the medium determines the message' be reconstructed when output is determined by software conditions such as model weights, data distributions, and prompt embeddings?

## Key Findings

### Reconstructing Kittler's Hardware Determinism in the Age of Generative AI: Toward Conditional Distribution Determinism

#### 1. The Core Structure of Kittler's Determinism

For Kittler, the 'message' of a medium is determined by the **material conditions of the sign**. His famous proposition "There is no software" (1992) argues that software is merely an illusion of hardware states. In *Gramophone, Film, Typewriter* (1986), Kittler argued that the kinds of data a medium can store, process, and transmit are **a priori limited** by its physical hardware:

> "Media determine our situation."

The phonograph can only process continuous acoustic signals, film only continuous visual images, the typewriter only discrete characters. Because this condition is given *a priori*, the medium itself determines the very range of possible messages.

#### 2. Three Levels of Challenge Posed by Generative AI

##### 2.1. Decentering Materiality: From Hardware to Distribution

In generative AI, the GPU is the material foundation of computation, but **it is not the GPU that determines the content of output.** Loading the same model weights on the same GPU with the same prompt produces the same output (when stochastic sampling is controlled). GPU architecture (H100 vs A100 vs TPU) creates performance differences but does not determine **what is output**.

The determining layers are rather:

| Layer | Determinative Power | Kittlerian Reducibility |
|-------|-------------------|------------------------|
| GPU Architecture | Boundary of computability | ✅ Hardware determinism possible |
| Model Architecture (Transformer) | Class of representable functions | ❓ Software, but implemented in hardware |
| **Training Data Distribution** | **Probability space of possible outputs** | ❌ Shift of determinative layer |
| **Model Weights** | **Concrete encoding of distribution** | ❌ Exist as data, not hardware states |
| Prompt/Embedding | Local conditions of output | ❌ User input, extra-medial factor |

The **training data distribution** determines the entire space of possible outputs (the stochastic latent space), and **model weights** encode that distribution. The 'limit of what can be stored' that Kittler spoke of is no longer a physical medium (grooves on a disc, photosensitive emulsion on film) but the **morphological characteristics of a statistical distribution**. Here, determinism shifts from 'hardware determinism' to **'distribution determinism.'**

##### 2.2. Redefining the Ontological Status of Software

When Kittler said "There is no software," he meant that every software state is ultimately reducible to a hardware state (register values, memory voltages). But in generative AI:

- **Model weights** are not reducible to a single hardware state. Billions of floating-point values are distributed across multiple GPUs, and their ontological status changes as they move across storage media (SSD → VRAM → cache).
- **Fine-tuning** changes only the weights while using the same hardware, same architecture, and same GPUs, yet produces a completely different output distribution. This means software-level changes exercise determinative power independently of hardware.
- The computation of **attention mechanisms** executes as GPU instruction sets, but the 'media effect' is more strongly determined by **architectural parameters** (number of layers, heads, embedding dimensions) than by the physical characteristics of the hardware (clock speed, memory bandwidth).

Therefore, Kittlerian reduction is insufficient to explain the determinative structure of generative AI. Software must be re-recognized as an **ontological layer with its own determinative power**, not a mere illusion.

##### 2.3. The Deterministic Paradox of Prompt and Stochasticity

The most intriguing point is the **position of the prompt**. Generative AI takes a user prompt as input and produces output. This appears to be a counterexample to Kittlerian determinism, since prompt engineering (e.g., chain-of-thought, few-shot) can dramatically change output.

However, the 'freedom' of the prompt is constrained as follows:
- The prompt is first **tokenized** into discrete units that the model can process — analogous to the keyboard determining characters in Kittler's framework.
- Tokenized prompts are mapped into an **embedding space** whose topological structure is entirely determined by the training data distribution. That is, what the prompt can 'mean' is only possible within the latent space that the training data has delineated.
- Temperature, top-k, and top-p sampling introduce **controlled stochasticity**, but this does not invalidate determinism. The stochastic process itself runs on a deterministic engine (**with a fixed seed, output is fully deterministic**).

The paradox of the prompt is this: **it appears as freedom to the user, but the very condition of possibility of that freedom is a priori constrained by the training distribution.**

#### 3. Reconstruction: Conditional Distribution Determinism

To reconstruct Kittler's hardware determinism effectively for the generative AI era, the following conditional shift is necessary:

> **Original proposition**: The medium (hardware) determines the kinds of data that can be processed/stored/transmitted.
> → **Output is constrained by the material conditions of hardware.**

> **Reconstructed proposition**: The training data distribution determines the topology of the model's latent space. Model weights are the encoding of this distribution, and output is a sampling of distribution-conditional probabilities.
> → **Output is generated by distributional conditions.**

This can be called **Conditional Distribution Determinism**:

```
P(output | prompt) ≈ argmax P(token_i | context < i, θ, D_train)
```

The determinative elements here are:
1. **D_train** (training data distribution) — determines the entire space of possible outputs
2. **θ** (model weights) — determines the encoding of the distribution
3. **Architecture** (Transformer attention mechanism) — determines the mode of relational computation
4. **Tokenizer** — determines the unit of symbolic discretization (the most Kittlerian layer)
5. **GPU** — determines whether computation is possible at all (the weakest determinative power)

#### 4. Kittler's Limitations and the New Media Conditions of Generative AI

Kittler's hardware determinism is invalid in generative AI for three reasons:

1. **Stratification of media layers**: Instead of a single 'medium,' a multi-layered stack (GPU + architecture + distribution + weights + prompt) exercises determinative power at different levels. A singular Kittlerian layer cannot explain this.

2. **Change in the ontological status of data**: For Kittler, data was 'content' stored in a medium. In generative AI, training data transcends stored content — it becomes the *a priori condition of possibility* for output. Data occupies the position of a Kantian transcendental condition.

3. **Introduction of stochasticity**: Kittler's media were deterministic (the phonograph reproduces what was input). Generative AI incorporates stochastic sampling as an essential element, and this 'controlled indeterminacy' becomes a core function of the medium.

#### 5. Connection to Khoj References

Khoj document 5 ("Kittler's Hardware Determinism and Generative AI — Toward a Conditional Shift to Distribution Determinism") aligns with the direction of this discussion, but its specific content could not be verified, making it difficult to use as direct evidence. Document 3 ("Narratology and Semiotics in the Age of Generative AI") discusses the **conflict between archive and matrix** — the stability of memory versus its fluidity — which connects to the conditional distribution determinism above: the structure in which the archive (fixed training data) becomes the condition of possibility for the matrix (fluid output generation) demonstrates how Kittler's separation of storage and processing is reconstructed in generative AI.

#### 6. Conclusion: "Distribution Determines the Condition"

Kittler's hardware determinism is **not directly valid** in the generative AI era, but the core of its deterministic insight — **the condition of possibility already determined before media use** — can be reconstructed in the form of **distribution determinism**. If Kittler said "media determine our situation," then for generative AI we can say:

> **"The training distribution determines the latent space of output. The medium (model) responds only within the range permitted by that distribution."**

Here, 'medium' is no longer a single hardware device but a **determination chain** connecting distribution → architecture → weights → tokenizer → GPU, where each link has a different ontological character of determinative power. This is the form of conditional shift that Kittlerian determinism must adopt in the generative AI era.

---

### Appendix: Limitations of the Reconstruction

This analysis has the following limitations:
1. It does not sufficiently reflect Kittler's later work (especially his shift from media archaeology to mathematical media theory). Kittler's own writings on digital media (e.g., the preface to the digital edition of *Aufschreibesysteme 1800/1900*) may contain clues to this problem.
2. The concept of 'distribution determinism' above has not yet been sufficiently formalized. Further theorization is needed to clarify how the 'condition of possibility' determined by distribution differs from Kant's transcendental conditions and Foucault's episteme.
3. If Khoj document 5 were available, contrasting its arguments could verify the validity of this reconstruction.

## Reference
- DeerFlow: 2026-07-12 21:00 KST | Model: DeepSeek V4 Flash
- Full analysis: /mnt/d/paper_md/생성논문/20260712210319_기술생성시대의 매체미학_1문항.md