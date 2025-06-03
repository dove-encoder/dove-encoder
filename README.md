# Images are Worth Variable Length of Representations

Authors: Lingjun Mao, Rodolfo Corona, Xin Liang, Wenhao Yan, Zineng Tang†

---

![DOVE Framework Overview](https://raw.githubusercontent.com/dove-encoder/dove-encoder/refs/heads/main/images/DOVE_Results_00.png) 

## Abstract

Most existing vision encoders map images into a fixed-length sequence of tokens, overlooking the fact that different images contain varying amounts of information. For example, a visually complex image (e.g., a cluttered room) inherently carries more information and thus deserves more tokens than a simple image (e.g., a blank wall). To address this inefficiency, We propose **DOVE**, a **D**ynamic **O**utput **V**ision **E**ncoder that produces a variable number of tokens to reconstruct each image. Our results show that DOVE significantly reduces the average number of tokens while maintaining high reconstruction quality. In several linear probing and downstream multimodal tasks, it outperforms existing autoencoder-based tokenization methods when using far fewer tokens, capturing more expressive semantic features compared to fixed-length encoding. We further extend DOVE with query-conditioned tokenization. By guiding the model to focus on query-relevant regions, it achieves more efficient and targeted semantic extraction.

## Contributions

1. We propose DOVE, a visual tokenizer that dynamically generates tokens based on image complexity. Unlike previous visual tokenization, our model supports arbitrary control over the token sequence length in a single parallel forward.
2. We propose a variant of DOVE that grounds token generation on a text query and its corresponding salient visual regions. This query-conditioned model achieves a higher token compression rate (averaging 68%) and demonstrates stronger semantic representation.
3. We observe a phenomenon of emergent semantics by probing the latent representation. Compared to other autoencoder-based tokenization methods with fixed-length token representations, our model achieves significantly better performance on classification, vision-language QA, and shows emerging semantic segmentation properties.
