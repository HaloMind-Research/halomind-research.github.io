---
layout: page
title: "Attention-Enhanced Swin Transformers for Robust Brain Tumor Classification Under Patient-Level Data Splitting"
permalink: /publications/swin-tumor/
---

### Abstract

Contemporary brain tumor classification systems report accuracies exceeding 98 percent, yet such metrics are artificially inflated by dataset partitioning flaws. Conventional image-level splitting allows identical patient scans in both training and testing sets, enabling networks to memorize patient-specific features rather than tumor patterns. We enforce patient-level separation where each patient remains in a single partition. Evaluation of five architectures reveals degradations reaching 3.71 percent under patient-level splitting, validating widespread data leakage. We propose an Attention-Enhanced Swin Transformer integrating hierarchical windowed attention with Convolutional Block Attention Modules. Our architecture achieves 96.82 percent accuracy with 1.23 percent degradation—the smallest gap among methods. Gradient-weighted activation mapping confirms attention on tumor regions rather than anatomical artifacts, establishing reliable feature extraction for trustworthy medical AI.


### Key Methodologies & Contributions
* **Algorithmic Patient-Level Partitioning:** Enforced strict patient-level separation where each patient's MRI scans remain in a single partition, eliminating data leakage that artificially inflates accuracy by 5-30 percentage points in conventional image-level splitting.
* **Attention-Enhanced Architecture:** Developed an Attention-Enhanced Swin Transformer that integrates hierarchical windowed attention with Convolutional Block Attention Modules (CBAM) to refine features through sequential channel and spatial attention.
* **Anatomical Artifact Suppression:** Utilized CBAM to explicitly prioritize tumor-discriminative features while suppressing patient-specific anatomical variations, such as skull boundaries and ventricular configurations.
* **Robust Generalization:** Achieved 96.82 percent classification accuracy under rigorous patient-level splitting, demonstrating a minimal performance degradation of 1.23 percent compared to image-level evaluation.

<br>
<a href="https://github.com/Latchan-Ch/Robust-Swin-Brain-Tumor" class="btn btn-outline">Code & Resources</a>

<hr>

**Status:** Accepted at IEEE GCON, 2026. **Authors:** L. Chhetri, A. Datta, P. Ghosal
