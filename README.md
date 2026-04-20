# GenMamba: Physics-Gated Generative Distillation for Frequency-Aware Real-Time Video Dehazing

> Official repository for **GenMamba**, a frequency-aware recursive framework for real-time video dehazing.

<p align="center">
  <img src="./assets/demo.gif" alt="GenMamba demo" width="800"/>
</p>

## Overview

Real-time video dehazing remains challenging because high-fidelity texture restoration often conflicts with efficient inference and temporal stability.  
GenMamba addresses this problem with a **frequency-aware recursive architecture** that combines:

- **Recursive Mamba / VSSD-based implicit alignment** for efficient spatiotemporal modeling
- **Dual-branch frequency decoupling** for stable structure recovery and texture enhancement
- **Physics-Gated Latent Distillation** to transfer generative priors while suppressing hallucinations
- **Alignment-Free Temporal Contrastive Regularization** for unsupervised training on real-world videos

GenMamba achieves strong perceptual quality and temporal consistency on real-world video dehazing benchmarks, while maintaining real-time efficiency.

## Highlights

- Real-time video dehazing with **32.4 FPS**
- More than **90% FLOPs reduction** compared with Transformer-based alternatives
- Strong temporal coherence without explicit optical flow alignment
- Physics-guided generative enhancement for realistic high-frequency detail recovery
- Effective unsupervised learning with non-aligned semantic reference matching

## Framework

GenMamba follows a teacher-student design:

- A **lightweight recursive Mamba student** performs efficient video dehazing
- A **frozen diffusion teacher** provides generative priors during training only
- A **Physics-Gated Latent Distillation** mechanism constrains generative guidance to degraded regions
- A **Low-Frequency branch** models structure and temporal consistency
- A **High-Frequency branch** restores textures via large-kernel refinement and cross-frequency interaction

## Demo

A qualitative demo is shown above.  
More visual results, failure cases, and downstream detection examples are provided in the paper and supplementary material.
