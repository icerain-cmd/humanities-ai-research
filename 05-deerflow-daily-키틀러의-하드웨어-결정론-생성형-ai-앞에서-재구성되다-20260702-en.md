# Daily DeerFlow Analysis: 2026-07-02

> Is Kittler's hardware determinism still valid in the media environment of the generative AI era? — How should the thesis that 'the medium determines the message' be reconstructed when output is determined by software-level conditions such as model weights, data distribution, and prompt embeddings?

## Question

Is Kittler's hardware determinism still valid in the media environment of the generative AI era? — How should the thesis that 'the medium determines the message' be reconstructed when output is determined by software-level conditions such as model weights, data distribution, and prompt embeddings?

## Key Findings

This question offers a crucial reexamination of Kittler's media theory under the new media conditions posed by generative AI. We analyze it systematically by contrasting Kittler's original claims with the challenges raised by generative AI.

---

### Kittler's Hardware Determinism — The Basic Structure

Kittler's famous thesis "There Is No Software" (1992/1997) consists of three layers:

1. **The Reduction Thesis**: All software-level operations are ultimately reducible to the voltage differentials (0/1) of transistor cells. No matter how abstract a programming language becomes, it ultimately terminates in physical state changes on silicon.

2. **The Concealment Thesis**: Software is a layer of abstraction — a "layer of concealment" — that hides the material conditions of hardware. The user's GUI, commands, and even assembly language all conceal the actual flow of electrons.

3. **The Determination Thesis**: The material conditions of the medium (hardware architecture) define the boundary between possibility and impossibility in information processing — this is the core of his declaration that "the medium determines the message."

Within this framework, Kittler asserts that "there is no such thing as software; only hardware exists." Even the CPU's microcode is merely the residue of "the last writing act" — the moment Intel engineers drew the 8086 layout across a 64-square-meter blueprint.

---

### The Challenge Posed by Generative AI — A Categorical Shift in Determinacy

However, generative AI (particularly Transformer-based LLMs) raises three fundamental difficulties for Kittler's analytical framework:

#### (1) The Locus of Determination Shifts from Hardware to Weight Space

For Kittler, determinacy originated from silicon's physical gate arrays. But what determines output in LLMs:

- **Model weights** (hundreds of billions of floating-point parameter matrices)
- **Training data distribution** (the statistical patterns of the corpus — itself already encoded cultural and linguistic conditions)
- **Prompt embeddings** (high-dimensional vectors into which input text is transformed)
- **Attention mechanisms** (software-defined dynamic selection of computational pathways)

All of these run on identical hardware (identical GPU, identical silicon), yet the decisive differences in output arise *not from hardware differences but from software-layer differences*. The fact that a fine-tuned Llama 3 and GPT-4 produce entirely different outputs on the same NVIDIA H100 GPU is due not to hardware but to **the composition of weight space** (training data, architectural design, learning algorithms).

This means that Kittler's determinacy remains valid at the **hardware ground level** but loses explanatory power at the **software overdetermination layer**.

#### (2) The Paradox of "No Software" — Weights Are Neither Hardware Nor Software

In Kittler's framework, all software is reducible to hardware. Yet LLM weight matrices disrupt this binary:

- On disk, weights are data (files); but when loaded into GPU memory during inference, they become **hardware's electrical state itself**.
- Simultaneously, weights are **statistically derived** values from training data via backpropagation — neither intended by hardware designers nor directly written by programmers.
- Thus, weights constitute **a third ontological category neither software nor hardware** — what might be called 'trained materiality' or 'statistical inscription.'

The "abstraction called software" that Kittler spoke of is in fact **a mediating term between hardware and data**. In the generative AI era, this mediating term has acquired its own determinative power.

#### (3) The Prompt Interface — An Inversion of the User-Medium Determinate Relationship

For Kittler, the user was a being subordinated to the material conditions of the medium ("we no longer write"). But the prompting interface of generative AI is paradoxical:

- The text input by the user (natural language) **directly alters the statistical conditions of output**.
- On identical hardware and identical weights, minute differences in prompts generate entirely different outputs.
- This appears as if the 'illusion of the subject' that Kittler criticized has returned — but in reality, it signifies that **hardware determinacy is now mediated by a software practice called prompt engineering**.

---

### Toward a Reconstruction of Kittler's Theory — A Three-Layer Model of Determination

Should Kittler's hardware determinism be entirely discarded in the generative AI era? No. Rather, it must be **reconstructed**. The following **multilayered structure of media determinacy** can be proposed:

```
[L3: Statistical Determinacy]
     - Distributional conditions of training data
     - Probabilistic structure of weight space
     - Determination at this layer: "which response has the highest probability"

[L2: Architectural Determinacy]
     - Computational conditions of the Transformer architecture (O(n²) attention complexity, context length limits)
     - Tokenizer segmentation
     - Determination at this layer: "what is possible/impossible"

[L1: Hardware Determinacy (Kittler's layer)]
     - Physical conditions of GPU/silicon (memory bandwidth, computational capacity, thermal output)
     - Energy and physical infrastructure of data centers
     - Determination at this layer: "what is executable/not executable"
```

Kittler's original thesis remains valid in that **L1 conditions L2 and L3 at the foundational level**. GPU memory capacity limits model size, which in turn defines the scope of representable knowledge. However, L2 and L3 possess **irreducible autonomous determinacy** — differences between GPT-4 and Llama 3 on the same GPU arise not from L1 but from L2/L3.

---

### Conclusion: Expanding 'Media Determinism'

In conclusion, Kittler's hardware determinism is **not entirely discarded** in the generative AI era, but it must be **substantially reconstructed**:

1. **Where it remains valid**: Kittler is still right — the geopolitical inequalities of GPU supply chains, the energy infrastructure of data centers, and the material conditions of semiconductor fabrication define the **foundational conditions** of what AI can and cannot do. This connects to the GPU geopolitics noted in the Machinocene flattening risk paper.

2. **Where reconstruction is needed**: However, Kittler's declaration that "the medium determines the message" must now be restructured from **single-layer determinism to multi-layer determinism**. If hardware constitutes the **necessary condition** of determination, then weight space and data distribution approach the **sufficient condition**.

3. **New theoretical challenge**: Generative AI has demonstrated that the layer Kittler dismissed as 'software' possesses its own **ontological thickness**. This demands a renewed discussion of the old Kittler–Hayles tension between material foundationalism and emergent patterns under new conditions.

4. **Connection to your research**: This issue connects to the irreducible tension between the 'foundational structure layer' and the 'representational structure layer' in Artificial Nature theory. Kittler's hardware corresponds to the foundational structure layer, while weight space and data distribution correspond to the representational structure layer. The **irreducible tension** between these two layers constitutes the media condition of generative AI.

## Reference
- DeerFlow: 2026-07-02 21:00 KST | Model: DeepSeek V4 Flash
- Full analysis: /mnt/d/paper_md/생성논문/20260702210343_기술생성시대의 매체미학_1문항.md