---
layout: page
title: "DeltaGate-CNN: A Lightweight Convolutional Architecture for Efficient Remote Sensing Image Classification"
permalink: /publications/ddv-mamba/
---

### Abstract
Real-time land cover classification on autonomous satellites requires models that are accurate, lightweight, and computationally efficient within strict hardware constraints. Vision Transformers and convolutional neural networks reach state-of-the-art results on benchmarks, but their quadratic self-attention cost and large numbers of parameters make them unsuitable for edge computing. We propose the DeltaGate-CNN (DG-CNN), a hierarchical architecture combining two mechanisms for edge deployment. First, a Gated Depthwise Aggregation module efficiently captures local spatial context. Second, we extend the Deep Delta operator to 2D feature maps, allowing each block to selectively erase redundant spectral data and write discriminative features using a channel-wise sigmoid gate. To assess deployment feasibility beyond pure accuracy, we define the Deployment Efficiency Score (DES = Accuracy × FPS / Parameters(M)), a multi-criteria score that balances model performance, speed, and efficiency. Assessed on EuroSAT, DG-CNN reaches 96.95% accuracy with 5.08 M parameters at 510 frames per second, achieving DES = 9733.2, a 13.1× relative improvement over ResNet50 (DES = 743.2) and 166.9× over ViT-B/16 (DES = 58.3). An ablation experiment validates the architectural necessity of the Deep Delta block, whose removal causes a 58.38 percentage-point accuracy collapse.


### Key Methodologies & Contributions
* **2D Deep Delta Operator:** Extended the Deep Delta operator from one-dimensional to two-dimensional spatial feature maps. This operator enables each block to erase redundant spectral data along a learned projection direction and write discriminative information.
* **SSM-Gated Aggregation:** Replaced quadratic self-attention with a State Space Model (SSM)-inspired gated aggregation module that utilizes depthwise convolution and channel-wise gating to restore global context at linear computational complexity.
* **Deployment Efficiency Score (DES):** Introduced a novel, hardware-centric compound metric that balances model classification accuracy, inference speed (FPS), and parameter count into a unified scalar value.
* **High-Throughput Edge Performance:** Reached 96.95% accuracy with 5.08 M parameters at 510 frames per second on the EuroSAT dataset. This resulted in a DES of 9733.2, achieving a 13.1x relative improvement over ResNet50 and 166.9x over ViT-B/16.
* **Architectural Ablation:** Conducted a controlled ablation experiment confirming that removing the Deep Delta block abolishes all residual connections and triggers a 58.38 percentage-point accuracy drop, validating its necessity as the architectural backbone.

<br>
<a href="https://github.com/HaloMind-Research/DDV-Mamba_for_Efficient_Remote_Sensing" class="btn btn-outline">Code & Resources</a>

<hr>

**Status:** Under Review at IEEE INDICON, 2026. **Authors:** L. Chhetri, A. Kumar, P. Ghosal
