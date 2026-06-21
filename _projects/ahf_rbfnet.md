---
layout: page
title: AHF-RBFNet
description: Attention-Guided Hierarchical Fusion U-Net with Learnable RBF Fuzzy Membership.
importance: 2
category: active research
---

### Architectural Engineering
[cite_start]In complex medical image segmentation (e.g., skin lesions), ambiguous boundary pixels degrade standard attention mechanisms[cite: 190]. [cite_start]We engineered AHF-RBFNet by replacing the traditional Gaussian fuzzy membership function with a learnable Radial Basis Function (RBF) kernel. 

[cite_start]**Gaussian Baseline:** $\exp(-((x - \mu) / \sigma)^2)$ [cite: 182]
[cite_start]**Proposed RBF Kernel:** $\exp(-\gamma \cdot (x - c)^2)$ [cite: 183]

[cite_start]Unlike standard deviations ($\sigma$) which can approach zero and destabilize training, $\gamma$ is a learnable parameter constrained strictly positive via a softplus activation[cite: 183, 185]. This provides numerically stable, boundary-aware spatial attention.

### Empirical Validation
* [cite_start]**Benchmark:** ISIC 2016 Skin Lesion Dataset[cite: 206].
* [cite_start]**Result:** Achieved 84.55% IoU and 91.97% Dice score[cite: 220].
* [cite_start]**Ablation:** Strictly outperformed 11 baseline architectures, including the original AHF-U-Net (UAFF) state-of-the-art variant[cite: 222, 223].
