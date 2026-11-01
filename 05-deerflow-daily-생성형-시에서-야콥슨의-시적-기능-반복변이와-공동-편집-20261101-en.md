# DeerFlow Daily Analysis: 2026-11-01

> What changes when Roman Jakobson’s proposition—that the poetic function generates meaning through the formal organization and self-referentiality of the message—is applied to an interactive poetry-creation environment in which generative AI produces different meters, line breaks, and chains of images each time from the same prompt? Argue which of stylistic repetition and variation constitutes the essential condition of the poetic function, and whether the user’s selection, revision, and regeneration constitute collaborative editing that forms the work’s formal unity, or an interpretive act that retrospectively renders the algorithm’s probabilistic variations literary...

## Question

What changes when Roman Jakobson’s proposition—that the poetic function generates meaning through the formal organization and self-referentiality of the message—is applied to an interactive poetry-creation environment in which generative AI produces different meters, line breaks, and chains of images each time from the same prompt? Argue which of stylistic repetition and variation constitutes the essential condition of the poetic function, and whether the user’s selection, revision, and regeneration constitute collaborative editing that forms the work’s formal unity, or an interpretive act that retrospectively renders the algorithm’s probabilistic variations literary.

## Analytical Results

# The Poetic Function and Generative-AI Poetry: A Theoretical Reconstruction of Formality, Authorship, and Variation

---

## 1. Framing the Problem — Examining the Conditions of a Theory’s Transfer

The central proposition of the poetic function formulated by Roman Jakobson in “Linguistics and Poetics” (1960) can be summarized as follows: “The poetic function projects the principle of equivalence from the axis of selection onto the axis of combination.” In other words, in ordinary language, items that can be substituted for one another—items belonging to the axis of selection—form relations of equivalence with adjacent items in poetry. As a result, the message becomes oriented toward itself: an “Einstellung toward the MESSAGE as such.”

When this proposition is transferred to an environment of generative-AI poetry creation, three elements must be fundamentally reconsidered:

1. **The subject of formal organization**: Who or what projects the principle of equivalence?
2. **The status of variation and repetition**: Of the different results produced from the same prompt, which constitutes the essential condition of the poetic function?
3. **The topology of user intervention**: How does the user’s selection, revision, and regeneration contribute to the work’s formal unity, and how does this differ from traditional authorship?

The following discussion uses the results of the Khoj literature search above—particularly the context of Document 5 on media aesthetics in the age of technological generation—as a primary reference.[^1] At the same time, it recognizes that the Khoj literature does not directly address this problem and therefore develops the answer through an independent theoretical construction.

---

## 2. The Statistical Transformation of Formal Organization — Who Projects the Principle of Equivalence?

### 2.1 The Poetic Function under Traditional Conditions

In Jakobson’s model, the poetic function presupposes the **intentional selection of the speaking subject**. The speaker selects items with particular phonological, syntactic, or semantic equivalences from the axis of selection and arranges them on the axis of combination through line breaks, meter, alliteration, and other formal devices. This selection and arrangement depend on the **formal judgment** of a willing subject. When a poet chooses “melancholy” instead of “sadness,” or “night” instead of “darkness,” this is not merely a lexical substitution; it is a decision made within a network of equivalences involving sound, meaning, and rhythm.

### 2.2 The Generative-AI Environment: “Selection” as a Conditional Probability Distribution

Systems such as PoeLM (2022), ByGPT5 (2022), and Jiuge-Tuiqiao (2026) produce different meters, line breaks, and chains of images each time they receive the same prompt.[^2] This means that **intentional selection has been replaced by probabilistic sampling**.

In the poetic generation of language models, “selection” operates as follows:

1. The prompt generates a distribution over possible tokens.
2. Probabilistic sampling occurs according to hyperparameters such as temperature and top-k.
3. The formal characteristics of the generated sequence—meter, syllable count, rhyme—are statistical reproductions of patterns learned during pretraining.

In this process, **the principle of equivalence described by Jakobson operates not through the will of a speaking subject but through the statistical distribution of the training data**. A poet’s choice of alliteration depends on a conscious sense of rhythm, whereas the AI model’s “alliteration” depends on the conditional probability of alliterative patterns within its training corpus.

**However**, this does not mean that the poetic function has disappeared; rather, it has been **transferred**. Ormazabal et al.’s PoeLM (2022), for example, explicitly assigns formal conditions by placing meter-control codes before the prompt.[^3] Here, the poetic function is reconstructed not through the will of a human subject but through the **three-way relationship among prompts, control codes, and probability distributions**.

---

## 3. Repetition and Variation — Which Is the Essential Condition of the Poetic Function?

### 3.1 The Status of Repetition in Jakobson’s Framework

In the traditional understanding of the poetic function, **repetition** is central: the regular recurrence of the same meter, the repetition of the same rhyme scheme, and the cycling of the same rhythmic pattern. Such repetition strengthens the self-referentiality of the message. The more the phrase “A rose is a rose is a rose” is repeated, the more language moves away from its referential function and draws attention to sound and form themselves.

### 3.2 Variation in AI Poetry: A Generative Condition

Yet the essence of the generative-AI environment lies in **generative variation**. Given the same prompt—“write a haiku about autumn rain”—the model produces a different output each time. Chen et al. (2024) point out that automatic poetry-generation systems are “considerably underdiverse,” while also demonstrating that **style-conditioned generation can substantially expand the range of variation**.[^4]

Here, the conditions of the poetic function are reversed:

| Traditional poetry | AI-generated poetry |
|-----------|-----------|
| Repetition is the essential condition of the poetic function | Variation is the essential condition of the poetic function |
| Equivalence is discovered within sameness | Equivalence is constructed within difference |
| The poet exercises intentional formal control | The user selects among probabilistic results |
| Form precedes and is filled with content | Form is discovered retrospectively within a set of variations |

**The significance of this reversal** is that, in the generative-AI environment, the operative condition of the poetic function is not “self-referentiality through repetition” but rather **“the capacity to retrospectively discover the poetic potential of the same prompt within variation.”** In other words, the poetic function resides not in the “output” but in the **selection process**.

[^1]: In particular, Document 5’s diagnosis—that “in the context of the age of technological generation, a gap appears that cannot be sufficiently captured by existing interpretive frameworks”—serves as the starting point for this analysis.
[^2]: Jiuge-Tuiqiao (Han et al., 2026) recognizes this problem and points out the limitation of the “one-shot generation paradigm,” in which the user is reduced to a “prompt provider.”
[^3]: PoeLM: “During inference, we build control codes for the desired meter and rhyme scheme, and condition our language model on them to generate formal verse poetry.”
[^4]: Chen et al. (2024): “Current automatic poetry systems are considerably underdiverse along multiple dimensions,” but “style-conditioning and character-level modeling clearly increase diversity.”

---

## 4. The Topology of User Intervention — Collaborative Editing or Interpretive Act?

### 4.1 The Dual Nature of User Selection

In generative-AI poetry creation, user intervention occurs at three levels:

1. **Prompt design**: Establishing the initial generation conditions
2. **Output selection**: Choosing one particular version from among multiple generated texts
3. **Revision and regeneration**: Altering a particular part of the selected output or generating a new version

Each of these three levels has a different status in relation to authorship.

**Prompt design** resembles the establishment of a theme in traditional poetic creation, but there is a decisive difference: when a poet selects a theme, they simultaneously consider formal possibilities—for example, whether to write a fourteen-line sonnet or a free-verse poem. Prompt design, by contrast, takes place in a state where the probabilistic result cannot be predicted.

**Output selection** is the theoretically most sensitive point. When a user chooses one poem from among ten generated poems, can this be understood as:

- (a) Collaborative editing? → The user does not directly intervene in the generation itself but merely selects a result.
- (b) An interpretive act? → Selection itself is not yet interpretation but rather differential approval.

**My position** is that this selection is a **precondition of interpretation**. Just as a reader who adopts a particular interpretation of a poem by C. Stevens is not thereby the producer or author of that poem, a user who selects one text from among AI outputs is not the author of the selected text. However, as Jiuge-Tuiqiao’s “triadic model (user-driven control, ancient-guided evidence, AI-assisted generation)” demonstrates,[^5] when the user locks specific words or phrases, receives real-time metrical feedback, and performs iterative refinement, this intervention moves beyond simple selection and becomes **genuine collaborative editing**.

### 4.2 The Interpretive Act of Retrospectively Rendering Algorithmic Variation Literary

I argue that the core of user intervention lies in **post-hoc literarization**. The grounds for this argument are as follows:

1. Texts produced by generative AI may appear statistically “poetic,” but they do not, in themselves, perform the poetic function. The poetic function is activated within a context in which the message is intended to draw attention to itself.

2. Only when the user selects one text from among numerous outputs and frames that selection with the assertion “this is a poem” does the text acquire the poetic function.

3. **This act of framing is an interpretive act.** Just as Duchamp’s readymades transformed everyday objects into art through the declaration “this is art,” the user transforms AI’s probabilistic output into literature through the judgment “this is a poem.”

4. However, when the user’s intervention includes **concrete revisions**—replacing words, changing line breaks, or adding particular images—that intervention simultaneously takes on the character of **collaborative editing**. Thus, depending on its depth, user intervention can be understood as follows:

   - **Low level of intervention** (simple selection): a post-hoc interpretive act
   - **High level of intervention** (locking, revising, resetting conditions): collaborative editing

   These are theoretical types rather than a strict empirical dichotomy. Most actual uses display continuity between the two statuses.

---

## 5. Synthesis — The Transformation of the Poetic Function in Generative-AI Poetry

### 5.1 The Reconstructed Relationship among the Three Elements

The changes that occur when Jakobson’s poetic function is applied to a generative-AI poetry environment can be summarized in the following diagram:

```text
Traditional conditions:
Poet (intentional selection) → Formal organization (projection of equivalence)
                            → Emergence of the poetic function

Generative-AI conditions:
Prompt (conditions) + Model (probability distribution) + User (selection/revision)
                              ↓
Generation of variations → User’s framing → Retrospective emergence
                           of the poetic function
```

The central transformations are:

1. **A reversal in the temporality of the poetic function**: before generation → after generation
2. **Repetition → variation**: a transformation of the operative condition
3. **The dispersal of authorship**: a single subject → a triadic relationship

### 5.2 Theoretical Implications

This analysis suggests that generative-AI poetry should not be viewed simply as a phenomenon in which “technology replaces poetry.” Rather, it should be understood as a moment in which **the ontological conditions of the poetic function itself are being transformed**. Jakobson’s poetic function has not disappeared. Its conditions of operation have merely been reconstructed through the **transformation of the conditions of technological generation**, in accordance with the diagnosis presented in Document 5.

In particular, the fact that the user’s selection, revision, and regeneration possess the **dual character of collaborative editing and interpretation** makes it impossible to define “authorship” in the age of generative AI in a linear or one-dimensional manner. AI poetry tools reveal a new form of poetic practice within a triadic relationship among the author’s intention, the statistical operations of the probabilistic model, and the user’s retrospective framing.

---

## 6. Limitations and Prospects

The Khoj literature consulted in this analysis does not directly address Jakobson’s poetic function. In particular, the relatively low semantic-similarity scores of the Khoj search results (0.109–0.148) suggest that the local literature database does not sufficiently cover the theoretical spectrum of the present question. For a more precise analysis, it will be necessary to obtain and examine additional studies that directly address Jakobson’s poetics and computational creativity—for example, Gervás (2009) and Lamb et al. (2021).

[^5]: The Jiuge-Tuiqiao system was designed to overcome the limitations of the existing “one-shot paradigm.” It allows users to lock phrases, receive real-time feedback, and perform iterative refinement. It therefore constitutes a concrete example of “collaborative editing” in the present discussion.

---

**References**

- Jakobson, R. (1960). “Linguistics and Poetics.” In T. Sebeok (Ed.), *Style in Language* (pp. 350–377). MIT Press.
- Chen, Y., Gröner, H., Zarrieß, S., & Eger, S. (2024). “Evaluating Diversity in Automatic Poetry Generation.” *arXiv:2406.15267*.
- Han, Y., Deng, L., Kong, C., et al. (2026). “Jiuge-Tuiqiao: An Interpretable Human-AI System for Classical Chinese Poetry Refinement.” *arXiv:2608.23098*.
- Ormazabal, A., Artetxe, M., Agirrezabal, M., Soroa, A., & Agirre, E. (2022). “PoeLM: A Meter- and Rhyme-Controllable Language Model for Unsupervised Poetry Generation.” *arXiv:2205.12206*.
- Belouadi, J., & Eger, S. (2022). “ByGPT5: End-to-End Style-conditioned Poetry Generation with Token-free Language Models.” *arXiv:2212.10474*.

## References

- DeerFlow: 2026-11-01 21:00 KST | Model: DeepSeek V4 Flash
- Full analysis: `/mnt/d/paper_md/생성논문/20261101210201_기술생성시대의 매체미학-기술생성시학_1문항.md`