# The Mechanistic Interpretability & Top-K Revolution (~2024–2025)

Spearheaded by teams at Anthropic and OpenAI, this revolution transitioned SAEs from generic feature extractors to precise microscopes for reverse-engineering Large Language Models.

## Core Mechanics
Researchers realized that an LLM's internal representation space contains millions of conceptual features wrapped inside an intertwined, compressed vector space (superposition). SAEs are trained directly over the intermediate activation layers of operational transformers to unwrap and extract thousands of distinct, human-interpretable features. 

This era standardized **Top-K SAEs** and **JumpReLU SAEs**, replacing smooth L1 penalties with hard mathematical constraints.

## Architectural Diagram
```mermaid
graph LR
    LLM[LLM Layer Activation] --> Input[SAE Input]
    Input --> Encoder[Encoder Projection]
    Encoder --> TopK[Top-K / JumpReLU Activation Selector]
    TopK --> Latent[Sparsified Latents (Only K Active)]
    Latent --> Decoder[Decoder Projection]
    Decoder --> Output[Reconstructed Activation]
```

## Signficance
This revolution enabled the discovery of monosemantic features, mapping abstract model activations to human-understandable concepts like code bugs, specific people, or abstract emotions.

[Back to README](../README.md)
