# DeerFlow Daily Analysis: 2026-09-30

> In cases where a smartphone photo app's automatic 'Memories' videos reconstruct the past by combining a user's deleted photos, location information, and music playback history, can digital memory be seen as operating not as the reproduction of preserved traces—as in traditional memory theory—but as an affective time produced by the platform? If so, how do the environmental costs of data and the user's right to be forgotten conflict in that reconstruction process?...

## Question

In cases where a smartphone photo app's automatic 'Memories' videos reconstruct the past by combining a user's deleted photos, location information, and music playback history, can digital memory be seen as operating not as the reproduction of preserved traces—as in traditional memory theory—but as an affective time produced by the platform? If so, how do the environmental costs of data and the user's right to be forgotten conflict in that reconstruction process?

## Analysis Results

# A Re-examination of the 'Memories' Feature of Smartphone Photo Apps from a Memory-Theoretical Perspective — An Eco-Digital View

## 1. Problem Statement: A Shift from Reproduction to Production

In traditional memory theory, memory has been understood as the retrieval of preserved traces (engrams). From Plato's wax tablet to Bergson's pure memory (*pure mémoire*), the authenticity of memory has been judged by whether it faithfully reproduces past experience. However, the automatic 'Memories' features of smartphone photo apps (Apple Memories, Google Photos Memories, etc.) fundamentally unsettle this premise.

The way this feature operates is as follows:
- (1) Database scan: It comprehensively scans photos and videos taken by the user, undeleted location metadata, and synchronized music playback history
- (2) Algorithmic selection: An ML model selects content based on 'significant moments' (face recognition frequency, location cluster size, temporal density)
- (3) Affective editing: It applies automatic transition effects, background music synchronization, and narrative structure (beginning-climax-resolution)

In this process, **the 'past' operates not as a reproduction of the user's memory but as an affective time produced by the platform**. The following sections examine the grounds for this claim.

---

## 2. Differences from Traditional Memory Theory — Three Transformations

### 2.1. Shift in the Agent of Selection (User → Algorithm)

The reproduction of memory in the traditional sense depends on the intentional recollection of the remembering subject. As Aristotle distinguished in *On Memory and Recollection*, memory (*mnēmē*) is mere retention, while recollection (*anamnēsis*) is active search. In the platform 'Memories,' however, selection is entirely delegated to the algorithm.

The user experience is more passive. In the case of Apple Memories, the user has not requested a specific memory; rather, the app automatically generates 'Memories of the Day' and presents them via notification. The user's role is reduced to that of an 'audience' who views them or hides them with an 'x' button.

### 2.2. The Novelty of Data Fusion

The platform's 'Memories' are constructed not from homogeneous material but through the fusion of heterogeneous data layers.
- Layer 1: Photos and videos taken by the user
- Layer 2: The device's location history (GPS logs)
- Layer 3: Playback history from music apps (Apple Music/Spotify integration)
- Layer 4: Temporal density (repeated visits to the same place and time)

This fusion produces **temporal relationships that the user has never individually experienced**. For example, a 'Memory' that combines photos taken in June 2024 with music played in June 2025 is a combination that never coexisted in the user's experiential time. This is a striking instance of what Friedrich Kittler identified as the situation in which **media themselves determine the conditions under which time is stored, processed, and transmitted**.

### 2.3. The Construction of Affective Time

The most important transformation is the affective reconstruction of time. Rather than simply displaying past data, the platform imposes a **narrative arc**.
- Opening: location panoramas, everyday scenes
- Development: person-centered clusters, shared moments
- Resolution: quiet landscapes, emotional release

This is not merely an automated version of video editing software, but rather **an algorithmic operation that extracts affective time from the database**. Here, time is no longer a re-presentification of the past but an affective object newly produced from data relations.

> **Preliminary Conclusion**: The 'Memories' feature of smartphone photo apps is difficult to capture with the reproductive model of traditional memory theory. It is an affective time produced by platform infrastructure, and the user is both the subject who consumes this time and the object who supplies its raw material.

---

## 3. Conflict with the Environmental Costs of Data

### 3.1. The Materiality of Infrastructure — An Eco-Digital Analysis

What the Eco-Digital perspective demands here is an analysis of the material conditions hidden behind the intangible experience of 'Memories.'

| Cost Type | Occurrence Stage | Specific Example |
|-----------|-----------------|------------------|
| Storage cost | Data centers | Cloud retention of all photos and metadata (deleted photos also retained for 30–60 days) |
| Computation cost | ML inference | Re-computation of face recognition, scene classification, and music matching when generating Memories |
| Transmission cost | Network | Streaming of thumbnails and video previews (via CDN edge nodes) |
| E-waste | Device replacement | The shortened life cycle of SoCs that support these services |

A key issue is that **even deleted photos retain their metadata for a certain period**. Even if the user intended to 'delete' them, the platform's memory reconstruction algorithm can continue to use that data. This has two environmental implications.

1. **Justification of surplus storage**: Despite the user's deletion intent, data is retained for algorithmic accuracy → increased energy consumption of storage infrastructure
2. **The circularity of computation**: Even if deleted data is not used in generating Memories, the original data may be needed for model retraining → increased pressure to retain all data

### 3.2. Tension with the Right to Be Forgotten

Here, the issue of the 'right to be forgotten' (*droit à l'oubli*) comes directly to the fore. The European Court of Justice's Google Spain ruling (C-131/12, 2014) and Article 17 of the GDPR, the 'right to erasure,' recognize an individual's right to demand the deletion of information concerning them. However, the 'Memories' feature of smartphone photo apps effectively neutralizes this right.

**Three dimensions of conflict:**

1. **Asymmetry of data retention**
   - User perception: Deleting a photo means the data disappears
   - System reality: Metadata of deleted photos (location, time, associated people) continues to be used by the Memories generation algorithm
   - GDPR perspective: Since 'complete deletion' does not occur, the substantive exercise of the right to be forgotten is impossible

2. **Affective coercion**
   - The 'Memories' generated by the platform reconstruct the past without considering the user's current emotional state
   - Affective coercion occurs when negative experiences (breakups, bereavement, loneliness) are repackaged as 'positive narratives'
   - Opt-out is possible (hiding specific people or dates), but this is only a post-hoc response

3. **The logic of commercial memory**
   - The 'Memories' feature is a commercial device designed to drive user engagement and return visits
   - The platform's memory production is a virtuous cycle of user retention and data accumulation
   - Forgetting is treated as an obstacle to the 'efficiency' of this structure

---

## 4. Implications of the Eco-Digital Perspective — Ontological Tensions

Taken together, the above analysis reveals three ontological tensions in the 'Memories' feature of smartphone photo apps.

### 4.1. The Duality of Time
- **Experiential time**: The time the user actually lived (Bergson's duration, *durée*)
- **Algorithmic time**: The affective object constructed from data relations
- Tension: The former is gravitational (unidirectional), while the latter is retroactive (retroactive recomposition)

### 4.2. The Fragmentation of the Subject
- The user is simultaneously a **memory consumer** (viewing generated Memories), a **data supplier** (providing raw material), and a **resistor** (hiding or deleting specific memories)
- This tripartite position ruptures the unitary subject presupposed by traditional memory theory

### 4.3. The Ecological Cost
- Behind the 'free' Memories feature lie the power consumption of data centers, broadband network traffic, and shortened device replacement cycles
- The Eco-Digital perspective demands that this material cost be integrated into memory-theoretical discourse

---

## 5. Provisional Conclusion

The automatic 'Memories' of smartphone photo apps constitute **an affective time produced from data relations** that cannot be adequately explained by the reproductive model of traditional memory theory. This is a new kind of technical memory phenomenon that can only be grasped by combining Kittler's media ontology, Simondon's individuation, and Stiegler's concept of tertiary retention.

At the same time, this feature exemplifies the structural tension between the environmental costs of data infrastructure and the right to be forgotten. The platform prioritizes algorithmic completeness and commercial effectiveness over the user's deletion intent, and in this process, **forgetting is treated as a 'bug' that undermines infrastructural efficiency**.

Ultimately, this case demonstrates that digital memory is no longer a matter of individual cognitive capacity or social practice, but rather a **techno-affective construct co-produced by media infrastructure and platform policy**. The task of Eco-Digital analysis is to make this construction process visible and to critically examine its material and ethical conditions.

---

### ※ Limitations of Using Khoj References

The Khoj local search results you provided (Yun Nara, "An Artistic-Engineering Understanding of Artificial Intelligence," 2020) focus primarily on the creativity of artificial neural networks and bias in facial recognition databases. As such, they do not provide direct evidence for the specific case of memory features in smartphone photo apps that this question addresses. However, indirect reference is possible in the following respects:

- The **correlation between database scale and algorithmic output** identified in the StyleGAN case analysis can serve as background for explaining why the Memories generation in photo apps requires massive data accumulation
- The discussion of the complementary relationship between connectionism and computationalism is useful for understanding the difference between the learning structure of ML models and traditional programming, but it does not directly connect to this analysis's argument about the memory-theoretical shift

Therefore, the above analysis is based primarily on theoretical reasoning and existing scholarly discourse (Kittler, Stiegler, Bergson, van Dijck, etc.), and the limited applicability of the Khoj results is clearly acknowledged.

## References
- DeerFlow: 2026-09-30 21:00 KST | Model: DeepSeek V4 Flash
- Full analysis: /mnt/d/paper_md/생성논문/20260930210408_에코 디지털_1문항.md