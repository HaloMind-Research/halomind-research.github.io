---
layout: page
title: "Optimizing Deep Learning for Brain Tumor Classification: A Comparative Ablation Study of Preprocessing and Augmentation Strategies"
permalink: /publications/brain-tumor-optimizing/
---

### Abstract
This work fills an important gap in the literature on brain tumor classification, where the overlap of patients between the training and test datasets has been artificially reducing reported accuracy. We have performed eight controlled experiments on 3,064 T1-weighted MRI images from 233 patients with strict patient-level splitting. Our ablation study compared skull stripping, CLAHE image enhancement, and bilateral filtering with geometric augmentation using VGG16 transfer learning. Our results show that skull stripping and CLAHE have a detrimental effect on accuracy when combined with augmentation (accuracy of 82 percent), while bilateral filtering with augmentation has an accuracy of 93.86 percent and AUC of 0.991 (p=0.05 compared to augmentation alone). We propose a new "destructive vs. constructive" taxonomy for image preprocessing, which indicates that image preprocessing techniques that preserve anatomical context are more effective than those that remove spatial information.


### Key Methodologies & Contributions
* **Strict Patient-Level Data Splitting:** Implemented an algorithmic split guaranteeing zero patient overlap across training, validation, and testing sets for 3,064 MRI images, eliminating the data leakage issue that artificially inflates accuracy by 5-30 percentage points in prior literature.
* **Comprehensive Preprocessing Ablation:** Executed eight controlled experiments isolating the effects of skull stripping, CLAHE image enhancement, and bilateral filtering paired with geometric data augmentation using a transfer learning VGG16 backbone.
* **Optimal Pipeline Configuration:** Discovered that bilateral denoising combined with data augmentation yields the optimal performance, achieving 93.86% accuracy and an AUC of 0.991 (p=0.05 compared to augmentation alone).
* **"Destructive vs. Constructive" Taxonomy:** Proposed a new preprocessing classification scheme demonstrating that context-removing methods (like skull stripping) severely degrade accuracy when combined with augmentation, while structure-preserving approaches (like bilateral filtering) enhance signal-to-noise ratios.

<br>
<a href="https://github.com/HaloMind-Research/Optimizing-Deep-Learning-for-Brain-Tumor-Classification" class="btn btn-primary">Code & Resources</a>

<hr>

**Status:** Accepted at IEEE GCON, 2026. **Authors:** L. Chhetri, A. Kumar
