# DeerFlow Daily Analysis: 2026-08-02

> Is Kittler's hardware determinism still valid in the media environment of the generative AI era? — How should the claim that "the medium determines the message" be reconfigured when output is determined by software conditions such as model weights, data distribution, and prompt embeddings?...

## Question

Is Kittler's hardware determinism still valid in the media environment of the generative AI era? — How should the claim that "the medium determines the message" be reconfigured when output is determined by software conditions such as model weights, data distribution, and prompt embeddings?

## Analysis Results

[Fallback Analysis: DeerFlow did not complete within the time limit, switching to direct analysis without MCP exploration]

# Media Aesthetics in the Technogenesis Era: Kittler's Hardware Determinism and the Software Conditions of Generative AI

## Introduction: Two Layers of Media Determinism

Friedrich Kittler's media theory brought about a decisive shift in media studies in the late 20th century. His famous thesis, "the medium determines the message," radicalized Marshall McLuhan's declaration by arguing that the material foundations of media—hardware, circuits, storage devices, transmission technologies—fundamentally constrain the form and content of possible information. For Kittler, media were not merely tools for transmission but the material conditions of information processing itself. This position was termed "hardware determinism" and became increasingly refined with the development of digital technology.

However, the explosive proliferation of generative AI since the 2020s tests Kittler's determinism in a new way. The output of generative AI is no longer directly determined by simple hardware conditions. Software conditions—model weights, data distribution, and prompt embeddings—play a decisive role in shaping output. This may appear as a fundamental challenge to Kittler's primacy of hardware. Is Kittler's determinism still valid in the era of generative AI? Or is a new media determinism needed that encompasses software conditions?

This paper combines three theoretical resources to answer this question. First, it examines the core thesis and limitations of Kittler's hardware determinism. Second, it introduces Gilbert Simondon's concept of concretization to explain the evolutionary process of technical objects. Third, by analyzing the synthetic data feedback loop and model collapse phenomenon in generative AI, it demonstrates that the evolution of technical objects can lead to regressive closure loops. Through this, it will ultimately argue that Kittler's determinism must be reconfigured to include software conditions, and discuss the implications of this reconfiguration for eco-digital or artificial nature research.

## 1. Kittler's Hardware Determinism: The Primacy of Material Conditions

Kittler's media theory begins with the concept of "discourse networks" (Aufschreibesysteme). In his book *Discourse Networks 1800/1900*, Kittler analyzed how media technology constitutes human knowledge systems. He argued that media are not neutral channels for transmitting information but themselves determine the form, storage method, transmission speed, and processing possibilities of information. This emphasizes the primacy of material conditions in a way distinct from the deconstructionism of American media scholar Paul de Man.

For Kittler, what was decisive was hardware—physical circuits, storage media, and transmission systems. For example, the phonograph made it possible to store sound as waveforms, and film decomposed visual continuity into frame units. Each medium inherently possesses a unique mode of information processing based on its physical structure, operating independently of user intention. Through this, Kittler presented a radical determinism that excludes human intentionality or subjectivity.

However, this approach has been criticized for not adequately considering the materiality of software. Software runs on hardware but possesses its own abstract logical structure and algorithmic determinacy. Kittler himself discussed software in his later works, but he still tended to regard software as a secondary phenomenon of hardware. This becomes a limitation when analyzing complex software systems like generative AI.

## 2. Software Conditions of Generative AI: Model Weights, Data Distribution, and Prompt Embeddings

To understand the operation of generative AI, it is necessary to distinguish three software conditions. Each plays a crucial role in reconfiguring Kittler's determinism.

**First, model weights** are parameters determined during the neural network's training process. As mentioned in the provided references, linear algebra is one of the mathematical fields that form the theoretical foundation of AI, and model weights are expressed through matrix operations. These weights are the result of compressing statistical patterns from large datasets, functioning as a kind of "recording device" in themselves. Borrowing Kittler's terminology, model weights function as a software-based storage device rather than a hardware one. However, they do not exist independently of hardware; they only gain meaning when executed on specific hardware architectures like GPUs or TPUs.

**Second, data distribution** refers to the statistical structure of the training data. Generative AI learns a specific data distribution and generates new samples that follow that distribution. Data distribution is not merely a statistical property but the result of epistemological and social decisions made during the selection, collection, and preprocessing of training data. Thus, data distribution reflects the social construction of media, an aspect Kittler overlooked.

**Third, prompt embedding** is the transformation of user input into a vector representation that the neural network can process. Prompt embedding shows the point at which user intention is converted into the machine's logical structure. In Kittler's determinism, human intention was subordinated to the material conditions of media, but prompt embedding serves as a medium through which user input determines output via software conditions.

These three conditions are interdependent. Model weights are the result of learning data distribution, and prompt embedding generates output through computation with these weights. This suggests a more complex causal relationship than Kittler's linear determinism. Hardware remains important, but its determinative power is mediated and transformed through software conditions.

## 3. Simondon's Concept of Concretization: The Evolution of Technical Objects

At this point, Gilbert Simondon's concept of the concretization of technical objects provides a useful analytical tool. Simondon views technical objects not as simple tools or machines but as organic entities evolving toward internal harmony. Concretization is the process by which abstract technical principles gradually acquire concrete form through material implementation.

Simondon's concept of concretization contrasts with Kittler's determinism. While Kittler sees the material conditions of media as fixed determining factors, Simondon sees technical objects evolving through interaction with their environment. In the early stages, a technical object exists as a collection of abstract components, but it gradually achieves functional integration and develops into a concrete individual.

Generative AI models well illustrate Simondon's process of concretization. Early neural network models were merely collections of simple layers, but with the emergence of the Transformer architecture and large-scale training, they gradually achieved complex functional integration. Model weights, data distribution, and prompt embeddings are not simple components but closely interconnected functional parts. This resembles the emergence of what Simondon calls a "technical individual."

However, Simondon's concretization is not a simple evolutionary process. He argued that true concretization occurs when a technical object internalizes functional conditions from its relationship with the environment. In the case of generative AI, training data constitutes the "environment" of the technical object. The model adapts to the environment by internalizing data distribution, which is a form of concretization. But this process also carries the risk of leading to a regressive closure loop.

## 4. Synthetic Data Feedback Loop and Model Collapse: The Possibility of Regressive Closure

A unique characteristic of generative AI is that it can use its own generated output as training data again. This is called the synthetic data feedback loop. It occurs when text, images, or code generated by the model are posted back on the internet and subsequently collected as training data for the model. When this loop is repeated multiple times, it leads to a phenomenon called model collapse.

Model collapse is a phenomenon where the diversity of generated data gradually decreases, eventually causing the model to produce only monotonous and repetitive output. This is similar to the process of species diversity decline in an ecosystem. Research shows that when synthetic data is repeatedly included in training data, the model gradually loses the tail of the original data distribution and becomes overly focused on the main modes. This means the model's output becomes increasingly limited and predictable.

This phenomenon demonstrates the possibility of a regressive closure loop, contrasting with Simondon's concept of concretization. If Simondon's concretization is an evolutionary process moving toward functional integration through interaction with the environment, the synthetic data feedback loop is a regressive process that blocks positive interaction with the environment and leads to internal closure. This reveals an irony: rather than being concretized through adaptation to the environment, the technical object loses sensitivity to the environment by repeatedly consuming its own output.

From this perspective, Kittler's determinism acquires new meaning. The claim that generative AI output is determined by software conditions acknowledges the existence of deterministic conditions beyond mere hardware. However, model collapse shows that these conditions are not static but dynamically change through feedback loops. In other words, software conditions are not fixed determining factors but variable conditions reconstituted by the model's output.

## 5. Evolution of Technical Objects and Regressive Closure Loops: A Comparison of Two Interpretations

The two processes discussed above—Simondon's concretization and the synthetic data feedback loop—offer two contrasting interpretations of the evolution of technical objects.

**First Interpretation: Evolutionary Concretization**  
Simondon's concretization is a process where a technical object achieves functional integration through close interaction with its environment. The development of generative AI partially supports this interpretation. Large language models (LLMs) have acquired increasingly sophisticated language understanding abilities through interaction with diverse data. In this process, models go beyond simple pattern matching to demonstrate contextual understanding, reasoning abilities, and a certain level of creativity. This can be compared to the internal harmony and functional integration of technical individuals that Simondon describes.

**Second Interpretation: Regressive Closure Loop**  
On the other hand, the synthetic data feedback loop shows a regressive process where the technical object refuses interaction with the environment and repeatedly consumes itself. This suggests that Simondon's concretization is not a simple evolutionary process but requires appropriate environmental conditions. Excessive use of synthetic data results in the technical object losing environmental diversity and becoming trapped within its own limits.

The two interpretations are not mutually exclusive. The current state of generative AI shows a complex dynamic where both processes coexist. On one hand, models have become capable of producing more sophisticated and diverse outputs, but on the other hand, the spread of self-generated data poses a long-term risk of reducing model diversity. This means that the evolution of technical objects occurs not through simple determinism but within a tension between open possibilities and the risk of closure.

## 6. Reconfiguring Kittler's Determinism: Media Determinism Including Software Conditions

Now, it is necessary to reconfigure Kittler's determinism for the era of generative AI. The core is to expand the claim that "the medium determines the message" from a hardware-centric view to one that includes software conditions.

The first step of reconfiguration is to expand the concept of media. For Kittler, media were material storage devices, transmission channels, and processing units. However, in generative AI, "media" should include software structures including model weights, data distribution, and prompt embeddings. This is the claim that the materiality of media is found not only in physical entities but also in algorithmic structures and statistical patterns.

The second step is to redefine the nature of determinism. Kittler's determinism assumed a linear causal relationship. However, in the case of generative AI, determinism is cyclical and feedback-based. Model weights determine data distribution, data distribution in turn determines model output, and output again affects data distribution. This requires a more complex dynamic determinism than Kittler's static determinism.

The third step is to reassess human intervention. Kittler viewed human subjectivity as subordinate to the material conditions of media. However, prompt embedding serves as a medium through which user input determines output via software conditions. This means that users can exercise a certain degree of choice within the constraints of software conditions. Of course, this choice is not complete freedom but the possibility of variation within the range permitted by software conditions.

Through this reconfiguration, the claim that "the medium determines the message" is transformed into the proposition that "software conditions determine the possibility space of output." This is more flexible than Kittler's radical determinism while still maintaining a deterministic character. Output is not completely free; it is constrained by software conditions. However, these constraints are more diverse and variable than hardware conditions.

## 7. Implications for Eco-Digital/Artificial Nature Research

This analysis provides important implications for eco-digital or artificial nature research. Eco-digital research is the perspective that digital technology forms systems similar to ecosystems and interacts within them. Generative AI can be considered a core component of this artificial nature.

**The first implication** is the possibility of self-organization in artificial nature. The feedback loop of generative AI resembles the cyclical processes of natural ecosystems. However, while natural ecosystems maintain stability through the interaction of diverse species, the synthetic data feedback loop risks losing diversity through model collapse. This suggests that artificial nature may have fundamentally different dynamics from natural ecosystems.

**The second implication** concerns the directionality of the evolution of technical objects. Simondon's concretization saw technical objects evolving through adaptation to the environment. However, in the case of generative AI, the environment (training data) is constituted by the output of the technical object itself. This means the technical object forms an auto-referential structure that creates its own environment. This is a new form of concretization that Simondon did not anticipate.

**The third implication** concerns the relationship between determinism and emergence. Kittler's determinism argues that the material conditions of media determine output. However, generative AI can exhibit unpredictable emergent properties through the interaction of complex software conditions. This shows that determinism does not exclude emergence. Despite deterministic constraints, various possibilities can emerge within those constraints.

**The fourth implication** is a practical proposal for convergence research between the humanities and AI. As mentioned in the provided references, AI workforce development policies tend to focus on technical aspects. However, the analysis in this paper shows that humanistic understanding—particularly media theory and philosophy of technology—is essential for the design and evaluation of AI systems. For example, preventing model collapse requires not only simple technical solutions but also maintaining diversity in data distribution, ensuring transparency in feedback loops, and recognizing the deterministic nature of software conditions.

## Conclusion: Toward a Media Aesthetics for the Technogenesis Era

This paper has explored whether Kittler's hardware determinism remains valid in the era of generative AI and how it should be reconfigured. In conclusion, Kittler's determinism should not be completely discarded but reconfigured to include software conditions. Hardware remains important, but its determinative power is mediated and transformed through software conditions—model weights, data distribution, and prompt embeddings.

Simondon's concept of concretization provides a useful framework for explaining the evolution of technical objects. Generative AI concretizes through interaction with its environment but simultaneously faces the risk of regressive closure through the synthetic data feedback loop. This means that the evolution of technical objects is not simple progress but occurs within a tension between open possibilities and the risk of closure.

Media aesthetics in the technogenesis era requires new conceptual tools capable of analyzing this complex dynamic. Kittler's determinism is no longer sufficient but should not be completely ignored. Rather, it should serve as a starting point for a more comprehensive theory that includes software conditions, feedback loops, and emergence. Such a theory can make significant contributions to eco-digital research and artificial nature research, providing humanistic insights for the design and evaluation of AI technology.

Finally, the argument in this paper is based on conceptual reasoning and proceeds without detailed empirical research or citation of specific papers. This reflects that the media-aesthetic analysis of generative AI is still an underdeveloped field. Future research will need to supplement this conceptual analysis with concrete case studies and empirical data.

---

**References**  
(This paper is based on the provided Khoj references and generally known theories, without directly citing specific academic papers. This is to clarify the nature of conceptual reasoning.)

## References
- DeerFlow: 2026-08-02 21:00 KST | Model: DeepSeek V4 Flash
- Full Analysis: /mnt/d/paper_md/생성논문/20260802210226_기술생성시대의 매체미학_1문항.md