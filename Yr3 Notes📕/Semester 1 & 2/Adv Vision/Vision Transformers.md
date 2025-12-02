# Vision Transformers
---
> [!info]- File Details
> Includes information about this (genus:: Note) from [Year::3]. Contains details on when this was created, what module the note belongs to.
> > *Date :*  27-11-2025
> > *Module :* [[Visual Computing]]
> > *Teacher*: 
> > *Resources :*

---
> [!abstract]+ Contents
> List of headings within this topic
> > [[#Speed run]]
> [[#]]


--- 
> [!tip]+ 🕰️* Speed run*
> Break down of topic 
> - Encoder only learn representation
> - Encoder-decoder learn translation (map a sequence)
> - Decoder only generate data in auto-regressive manner
> - Masked Self-Attention means no cheating via future look ups. attention to future tokens are masked/blanked out 
> - why use ViT over CNN even w worse inductive bias??? 
> 	- Bcos of Scale  - larg scale training trumps inductive bias. 
> 	- Long-Range Dependencies - Using self attentions to relate opposite ends of images. 
> 	- Multimodality - basically NLP models, hence ez to build systems understanding text an images
> - Swin Transformer tries to combine both Vit and CNN with window based attention
> - Cross attention is self attention but with queries coming from the decoder 
> - Key Terms: Vision Transformer, Cosine Classifier, L2 Normalization, Triple Loss, Class Centres, Self-Attention, Encoder, Decoder, Attention Weights, Scaled Dot Product Attention, Positional Encoding, Multiple Heads, Masked Self-Attention, Cross Attention, Inductive Bias, Translation Invariance, Locality, Hierarchical Composition, CNN, Multi-modal Learning, Foundation Models, Image Patch Embeddings, Class Embedding, Positional Encoding Learning, Self-Attention Efficiency, Swin Transformer, Multi-Scale Attention.


### CNNs vs. ViTs: Inductive Bias

The lecture highlights a critical trade-off between Convolutional Neural Networks (CNNs) and Transformers.
- **Inductive Bias:** This refers to the assumptions built into a model to help it generalize.
    - **CNNs:** Have **high** inductive bias. They assume translation invariance (the same feature can appear anywhere) and locality (pixels near each other are related). This helps them learn well with smaller datasets.
    - **ViTs:** Have **low** inductive bias. They process the image globally. The only spatial structure comes from cutting the image into coarse patches.

**Why use ViTs if they have worse inductive bias?**
1. **Scale:** "Large scale training trumps inductive bias." With enough data, ViTs outperform CNNs.
2. **Long-Range Dependencies:** ViTs can relate pixels at opposite ends of an image instantly via self-attention, which is great for complex scene understanding.
3. **Multi-modality:** Because the architecture is nearly identical to NLP models, it is easier to build systems that understand both text and images (e.g., CLIP).
---

![[Transformer Block.png]]


1. Vision Transformers (ViTs)
2. Cosine Classifier
3. L2 Normalized Embeddings
4. Triple Loss
5. Class Centres Update Mechanism
6. Self-Attention Mechanism
7. Encoder-Decoder Architecture
8. Transformer Models
9. Attention Weights
10. Scaled Dot Product Attention
11. Query, Key, and Value Representations
12. Positional Encoding
13. Multiple Attention Heads
14. Masked Self-Attention
15. Cross Attention
16. Inductive Bias in Machine Learning
17. Translation Invariance
18. Locality and Hierarchical Composition
19. Limitations of CNNs vs. ViTs
20. Importance of Large Datasets in Training ViTs
21. Multi-modal Learning and Foundation Models
22. Structure of the Vision Transformer Pipeline
23. Image Patch Embeddings
24. Class Embedding in ViTs
25. Learning of Positional Encodings in ViTs
26. Efficiency of Self-Attention in ViTs
27. Swin Transformer and Multi-Scale Attention