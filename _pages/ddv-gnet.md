---
layout: page
title: "DDV-GNet: High-Throughput Defect Detection for Space Manufacturing via Deep Delta Gated Networks"
permalink: /publications/ddv-gnet/
---

### Abstract

Real-time defect detection for space manufacturing and satellite components' quality control necessitate processing rates beyond 600 frames per second with high classification accuracy under severe computational constraints. State-of-the-art deep learning models face an inherent problem, where convolutional neural networks like ResNet50 achieve high accuracy but fall short of satisfying real-time constraints for synchronized production lines, while efficient models compromise on detection accuracy. In this paper, we propose a novel hierarchical gated convolutional architecture called Deep Delta Vision Gated Network (DDV-GNet) that resolves the inherent problem of existing models by achieving high accuracy with linear complexity processing and hardware-optimized design. Our proposed model uses gated linear transformations with Deep Delta operators across eight specialized blocks divided into four stages with progressive feature expansion from 64 to 512 dimensions. Our proposed model achieves 87.91% classification accuracy with 7.18M parameters on the PVEL-AD dataset with 12 unique solar panel defect classes while processing at 853.94 FPS with 1.17 ms latency on NVIDIA T4 hardware. To the best of our knowledge, DDV-GNet is the only architecture exceeding processing rates beyond the critical 600 FPS industry deployment rate with 35% lower latency than EfficientNet-B0 and 12× speedup over competing Vision Transformer models with comparable accuracy. These results establish that gated convolutional networks enable practical deployment of AI-powered quality control systems in resource-constrained aerospace manufacturing environments where real-time decision-making directly impacts mission success.


### Key Methodologies & Contributions
* **Hierarchical Gated Architecture:** Designed a four-stage hierarchical convolutional network with progressive dimension expansion from 64 to 512. It employs gated convolutional dynamics for data-dependent feature filtering, effectively bypassing the quadratic complexity bottlenecks of standard self-attention mechanisms.
* **Deep Delta Operator:** Introduced a novel feature integration mechanism that boosts gradient flow across the network. It models the difference between input states and processed features using a multiplicative delta rule, mathematically defined as delta = (x \c.k) + v, ensuring stable optimization.
* **Domain-Adaptive Pre-training:** Replaced standard ImageNet initialization with EuroSAT satellite imagery weights. This domain-specific transfer learning leverages relevant textural patterns, boosting validation accuracy by 1.8% on the PVEL-AD dataset.
* **Ultra-High Industrial Throughput:** Achieved an inference speed of 853.94 FPS with a latency of 1.17 ms on standard NVIDIA T4 hardware. This explicitly shatters the critical 600 FPS threshold required for synchronized real-time aerospace manufacturing lines.
* **SOTA Efficiency-Accuracy Trade-off:** Delivered 87.91% classification accuracy across 12 highly imbalanced solar panel defect classes with a lightweight footprint of just 7.18M parameters. This maintains linear computational complexity while operating 12x faster than competing Vision Transformer models.
<br>

<a href="https://github.com/HaloMind-Research/DDV-GNet-Space" class="btn btn-primary">Code & Resources</a>

<hr>

**Status:** Accepted for Oral Presentation at IEEE SPACE, 2026. **Authors:** L. Chhetri, A. Kumar 
