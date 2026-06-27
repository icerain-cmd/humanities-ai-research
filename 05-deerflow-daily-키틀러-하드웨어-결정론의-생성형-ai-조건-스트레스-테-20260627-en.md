# Daily DeerFlow Analysis: June 27, 2026 (Sat)

> Stress-testing Kittler's hardware determinism under generative AI conditions

## Question

Is Kittler's hardware determinism thesis from *Grammophon Film Typewriter* (1986)—that the physical conditions of media *a priori* determine the form of possible discourse—still valid in environments like DALL-E 3 or Stable Diffusion, where identical GPU hardware runs software-level conditions (model weights, data distribution, prompt embeddings) that actually determine the form and content of outputs? If hardware determinism is to be maintained, what modifications to Kittler's theoretical framework are necessary?

## Key Findings

# Stress-Testing Kittler's Hardware Determinism Under Generative AI Conditions

---

## 1. A Precise Reconstruction of Kittler's Hardware Determinism

Before analysis, Kittler's thesis must be decomposed into three levels.

**(L₀) Ontological Level**: Hardware materiality constitutes the condition of possibility for discourse. The preface to *Grammophon Film Typewriter*—"Medien bestimmen unsere Lage" (Media determine our situation)—is not merely a claim about social influence but a transcendental *a priori* claim. The phonograph's acoustic recording converts sound (wave) into physical grooves, and the shape of these grooves **a priori** limits the range of possible listening experiences. Similarly, film's frame rate (24fps), the grain size of film's silver halide particles, and the typewriter's keyboard layout each pre-determine the form of possible visual and textual experience at the material level.

**(L₁) Epistemological Level**: Hardware conditions determine the *form of knowledge* that can be known. For Kittler, *Aufschreibesysteme* (discourse networks, 1800/1900) are not merely recording technologies but **the medial *a priori* of the unconscious**. The phonograph-cinema-typewriter system around 1900 formed a feedback loop that made human perception itself an object of technology—and only within this loop did psychoanalysis, film theory, and psychophysics become possible.

**(L₂) Software Positioning**: For Kittler, software is merely the "shell" of hardware. In *There Is No Software* (1992), he argues that all software operations are ultimately reducible to the physical gates and clock cycles of the microprocessor. The concept of "software" itself is an ideological device that conceals the materiality of hardware.

These three levels are challenged in different ways under generative AI conditions.

---

## 2. The Technical Conditions of Generative AI: Identical Hardware, Variable Software

The technical architecture of generative AI image models can be reconstructed at the same level of analysis:

| Component | Function | Determinant Variable |
|-----------|----------|---------------------|
| GPU Hardware (H100/A100) | Tensor operation acceleration, memory bandwidth | SM count, memory capacity (80GB), tensor core TFLOPS |
| CUDA/cuDNN Driver | GPU abstraction layer | Computational graph optimization |
| Model Architecture (U-Net, DiT) | Defines latent space topology | Parameter count, attention mechanism, diffusion trajectory |
| Training Data Distribution | Defines probabilistic distribution of possible outputs | Dataset composition, captioning strategy, filtering |
| Prompt Embedding | Semantic vectorization of conditional input | Embedding model (CLIP, T5), tokenization |
| Sampling Parameters | Controls generation process | CFG scale, sampler, steps, seed |

**Core Issue**: On the same H100 GPU, Stable Diffusion XL, DALL-E 3, FLUX.1, and PixArt-α produce entirely different visual forms and contents. If Kittler's L₂ thesis (software = shell) were true, outputs on identical hardware should be structurally homogeneous. But reality shows otherwise.

This is demonstrated by three levels of **formal difference**:

**(1) Formal Difference—Resolution and Aspect Ratio**: SDXL has 1024×1024 as its native resolution, while DALL-E 3 supports variable resolutions (1792×1024, 1024×1792). On the same GPU performing identical tensor operations, the spatial embedding strategy at the architecture level determines the **formal dimension** of the output.

**(2) Stylistic Difference—Distributional Bias**: On the same GPU with the same "a cat" prompt, SD 1.5, SDXL, and DALL-E 3 display different stylistic preferences (expressionist realism, flat minimalism, photorealism). This means the data distribution (statistical *a priori*) overrides the hardware's material *a priori*.

**(3) Ontological Difference—The Mode of Being of the Image**: SDXL generates RGB raster images, while DALL-E 3 generates images through token sequences. The latter follows the LLM's sequence-to-sequence paradigm, which changes the **ontological status** of the image itself. Different ontologies on identical hardware.

→ This suggests that even at the L₀ level, hardware determinism is difficult to maintain. But discarding Kittler too easily would be a theoretical waste. Let us now apply Kittler's framework **more precisely**.

---

## 3. Attempting Kittler's Rehabilitation: Reading the GPU as a Medium

To apply Kittler's logic consistently to generative AI, the following claim is possible:

**"The GPU is not merely a computing device but a medium that determines the *a priori* form of possible images."**

The GPU's core operations are **matrix multiplication** and **tensor contraction**. These constitute the material-mathematical foundation shared by all current generative AI systems. That is:

- Every generated image is a **visualization of tensor operations**
- Each step of the diffusion process is a chain of FP16/BF16 matrix multiplications performed on the GPU's tensor cores
- The space of possible images is materially constrained by GPU floating-point precision and memory bandwidth

From this perspective, Kittler's L₀ can be **redefined** as follows:

> **Revised L₀'**: The GPU's tensor core architecture is the **computational *a priori*** that all generative images must pass through. The pixel values of generated images cannot escape the materiality of floating-point quantization, and memory limits physically constrain the dimensions of the latent space.

This is true—an FP16-represented image can have subtle color differences from an FP32-represented image, and GPU memory (80GB H100) physically limits maximum batch size and resolution. However, this claim has **significantly less explanatory power** than Kittler's original thesis.

When Kittler analyzed the transition from camera obscura to photography in *Optical Media* (1999), he showed not a mere change in computational capacity but how **a change in the physical recording of light** restructured visual discourse. The transition from the simple pinhole of the camera obscura to the lens-film complex changed recognizable reality itself.

Does the GPU's tensor core correspond to such a **medial switch**? That is, does the GPU create qualitatively different medial conditions from previous computing hardware (CPU, DSP)?

The answer is **ambiguous**. The GPU's tensor operations are ontologically continuous with the CPU's scalar operations (both are variants of the von Neumann architecture). Analog media (phonograph-cinema-typewriter), by contrast, each used qualitatively different physical processes (acoustic-optical-mechanical). For Kittler, the determinacy of media originated in **physical heterogeneity**, and the GPU replaces this heterogeneity with digital universality.

This is the core difficulty for Kittler's theory. Every image generated on a GPU is the output of the same physical process (electron flow → Boolean operations → floating-point calculations), which is qualitatively homogeneous compared to the difference between the phonograph's acoustic grooves and film's silver halide grains.

---

## 4. Necessary Theoretical Modifications: Three Proposals

### 4.1 Proposal 1: Stratified Mediatric Determinism

Kittler's single-layer hardware determinism must be extended to **n-layer determinism**. Each layer has its own 'medial *a priori*', and the autonomy of upper layers is only partially constrained by the material conditions of lower layers.

```
L₃: Prompt/User Input    →  Semantic/Discursive Determinacy
L₂: Training Data Dist.   →  Statistical/Probabilistic Determinacy  ← NEW
L₁: Model Architecture    →  Topological/Structural Determinacy     ← NEW (software medium)
L₀: GPU Hardware          →  Computational/Material Determinacy
```

The degree and nature of determinacy differs at each layer:
- L₀: **Strong determinacy** (constrains output through physical impossibility—tensors exceeding 80GB cannot be generated)
- L₁: **Medium determinacy** (architecture defines the space of possible functions, but variation within that space is nearly infinite)
- L₂: **Weak determinacy** (distribution grants probabilistic tendencies, but external factors enable continuous change)
- L₃: **Minimal determinacy** (user input provides semantic direction, but output still depends on L₁/L₂ statistical characteristics)

Kittler considered only L₀, but in generative AI environments, **L₁ and L₂ exert greater influence on output determination than L₀**. This demands not the abandonment of hardware determinism but its **vertical redistribution**.

### 4.2 Proposal 2: Mediation Through Flusser's Concept of Technical Images

Vilém Flusser, in *Towards a Philosophy of Photography* (1983) and *Kommunikologie* (1996), presented a media theory similar to but distinct from Kittler's. For Flusser, the photograph (prototype of the technical image) is produced by an **apparatus**—an automated device that mediates and transforms human intention. The operator can only choose within the range allowed by the apparatus's internal program, and the apparatus becomes increasingly autonomous.

This applies directly to generative AI:

- Flusser's 'apparatus' → diffusion model (architecture + weights)
- Flusser's 'program' → training data distribution + sampling parameters
- Flusser's 'operator' → prompt engineer
- Flusser's 'technical image' → AI-generated image

The crucial point for Flusser is the **black-boxing of the apparatus**. The photographer shoots without understanding the physical process of lens and film, and this ignorance strengthens the apparatus's power. In generative AI, the user inputs prompts without understanding the GPU's tensor operations (the black box), and the internal diffusion process is concealed by the sampler.

Flusser's framework **fills the theoretical gap** between Kittler's hardware determinism and software freedom: hardware still sets the material conditions, but on top of those conditions, the apparatus's program (software + data) exercises substantive determinacy. If Kittler emphasized the **material unconscious** of media, Flusser emphasizes the **computational unconscious** (the opacity of algorithms) of media.

> **Modified Proposal**: Kittler's hardware determinism must be **combined with Flusserian apparatus theory**. Hardware determinism is not negated, but determinacy at the 'program' layer projected by the apparatus is added. Final determinacy arises from the hardware+software+data complex.

### 4.3 Proposal 3: Historicization Through Stiegler's Tertiary Retention

Bernard Stiegler, in *Technics and Time* (1994–2001), extends Kittler's media determinism in a different direction. For Stiegler, technics constitutes **tertiary retention**—an externalized memory storage that goes beyond individual experience (primary retention) and collective oral tradition (secondary retention). Writing, photography, recording, and digital data are all forms of tertiary retention.

In generative AI, the **training dataset** is a vast tertiary retention. Stable Diffusion's LAION-5B dataset contains billions of image-text pairs collected from the internet, and the **historical and cultural composition** of this dataset fundamentally determines the model's output.

From Stiegler's perspective, what Kittler overlooked is the **historical dimension of media**:
- Kittler's hardware operates **synchronically**—material conditions at a specific point in time determine discourse
- Stiegler's tertiary retention operates **diachronically**—the historical accumulation of data determines output

In generative AI environments, this diachronic dimension is decisive. SD 1.5 and SDXL operate on the same GPU, but SDXL's expanded training data (more high-resolution images, more sophisticated captioning) produces qualitative differences in output. This difference stems not from hardware but from the **history of data**.

> **Modified Proposal**: Kittler's hardware determinism must be **combined with Stiegler's theory of tertiary retention**. The determination of output arises from a **dual determination** of synchronic material conditions (hardware) and diachronic data conditions (the historical composition of training data).

---

## 5. Theoretical Stress Test Results: Comprehensive Assessment

| Kittler's Layer | Validity Under Gen AI Conditions | Modification Required |
|--------------|-------------------------------|---------------------|
| L₀ (Material a priori) | **Partially valid**—GPU computational/memory limits still act as material constraints | Requires redefinition as tensor core medium |
| L₁ (Epistemological a priori) | **Vulnerable**—software layer determines output form independently of hardware | Requires layer differentiation (stratification) |
| L₂ (Software = Shell) | **Invalid**—software is not a shell but a determinative media layer | Requires comprehensive revision |

**Final Verdict**: Kittler's hardware determinism is **not valid as a standalone thesis** in generative AI environments. However, what is needed is not wholesale abandonment but **structural expansion**.

### 5.1 Key Required Modifications

**(1) Extension from Single-Layer to Multi-Layer Model**
Hardware determinism should be retained, but software (model architecture, training data, prompting) must be recognized as independent determinative layers. Kittler's error was reducing diverse levels of determinacy to a single one (L₀).

**(2) Redefinition of Medial Parameters**
Kittler's media operated through qualitatively different physical processes (sound→grooves, optics→silver halide). Generative AI media produce all outputs through the same physical process (electrons→Boolean→floating-point). This universality is a new media condition that Kittler's original framework did not anticipate. Therefore, **media determinacy should be sought not in the specificity of physical processes but in the variables of computational processes (architecture, distribution, prompt)**.

**(3) Introduction of the Historical Dimension**
Kittler's synchronic analysis fails to capture the diachronic determinacy of generative AI (the history of data, model training history, updates). Stiegler's concept of tertiary retention should be introduced to integrate the historicity of data into media theory.

---

## 6. Conclusion: Toward an Ontology of Tensor Images

Kittler's hardware determinism faces a fundamental challenge under generative AI conditions, but it should not be entirely discarded. Rather, the fundamental question Kittler raised—**"How do the material conditions of media *a priori* determine the possibilities of experience and discourse?"**—has become even more important in the generative AI environment.

The direction of the answer must change, however. Instead of Kittler's single-layer hardware determinism, I propose the following **extended Kittler thesis**:

> **Extended Thesis**: In generative AI environments, the form and content of outputs are determined by a **complex multi-layer determination** of GPU hardware (material *a priori*), model architecture (topological *a priori*), training data distribution (statistical *a priori*), and prompt conditioning (semantic *a priori*). Hardware still provides the material foundation, but the most influential determinative layers have shifted from hardware to model architecture and data distribution.

This modification preserves Kittler's spirit—**taking the materiality of media seriously**—while capturing the complexity of generative AI as a new medial condition. Ultimately, what we need is neither Kittler's abandonment nor his blind acceptance, but a **third-generation model of media theory**—a framework integrating the triple determinacy of hardware, software, and data.

---

## Reference
- DeerFlow: 2026-06-27 21:00 KST | Model: DeepSeek V4 Flash
- Full analysis: /mnt/d/paper_md/생성논문/20260627210647_기술생성시대의 매체미학_1문항.md