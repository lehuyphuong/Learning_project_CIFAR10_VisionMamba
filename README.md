# Learning Project: VisionMamba on CIFAR-10
> This project is a hands-on learning implementation of Vision Mamba (Vim)—an emerging vision backbone based on State Space Models (SSMs)—adapted for the CIFAR-10 image classification task.

## Project Structure
```
|__ main.ipynb
└── README.md                         # This documentation
```

## Vision Mamba: Core Idea (Concept)
Vision Mamba (Vim) proposes a pure SSM-based vision backbone, replacing traditional self-attention mechanisms found in Vision Transformers (ViTs) with bidirectional Mamba blocks and positional embeddings to efficiently model global and positional dependencies.  

Key Concepts:
- Patch Tokenization with Positional Awareness:  
Images are divided into patches, flattened, and linearly projected into token embeddings, with positional embeddings added—similar to ViT but using SSMs to process the sequence
- Bidirectional State Space Modeling:  
Instead of using attention, Vim processes the token sequence with bidirectional state space blocks that aggregate context from both directions, enabling efficient global representation
- Efficiency Gains:  
Vim achieves faster inference speeds (e.g., ~2.8× faster than DeiT) and significantly reduced GPU memory usage (up to ~86.8% less) on high-resolution tasks  

## VisionMamba on CIFAR-10
**Objective**: Learn how Vision Mamba works by implementing the core idea in PyTorch, focusing on CIFAR-10 (32×32 images, 10 classes).  
**Scope**:  
- Design a simplified bidirectional Mamba block
- Wire a minimal forward pass suitable for classification  
**No training results**: this is a learning and architecture exploration project via a single Jupyter notebook.  

## Notebook
Open [main.ipynb](main.ipynb) to explore

## Acknowledgements
[Vision Mamba (Vim)](https://arxiv.org/abs/2401.09417): Efficient Visual Representation Learning with Bidirectional State Space Model (Zhu et al., 2024)