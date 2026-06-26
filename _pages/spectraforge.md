---
layout: page
title: "SPECTRAFORGE: Domain-Equalized Frequency-Spatial Fusion for Synthetic Dermatology Detection"
permalink: /publications/spectraforge/
---

### Abstract

Spatial deepfake detectors in medical imaging typically exploit dataset-level flaws, such as JPEG compression history, edge statistics, and color biases, rather than identifying authentic generative footprints. Consequently, these models suffer severe performance degradation when evaluated on images from unseen generators. To address this vulnerability, we introduce SPECTRAFORGE, a two-stream CNN framework that explicitly decouples the detection task. A Gaussian-bottlenecked spatial stream isolates macroscopic lesion morphology, while a parallel FFT-magnitude stream maps the periodic upsampling artifacts inherently produced by diffusion decoders. Prior to training, our Extreme Equalizer preprocessing pipeline systematically eliminates dataset spatial leakage. Evaluated on a strictly controlled 2,000-image forensic cohort, SPECTRAFORGE yields an AUC of 0.9971 ± 0.0016 and a Precision of 0.9931 ± 0.0056 across three-seed cross-validation, outperforming the EfficientNet-B0 baseline across all metrics. Crucially, under cross-checkpoint out-of-distribution (OOD) stress testing, EfficientNet-B0 suffers catastrophic domain collapse (AUC dropping to 0.5494), whereas SPECTRAFORGE maintains robust detection capabilities (AUC 0.9277). This +0.3783 AUC margin demonstrates strong frequency-domain generalization, while Grad-CAM and t-SNE projections on the OOD data visually confirm the successful decoupling of clinical anatomy from synthetic artifacts.


### Key Methodologies & Contributions
* **Extreme Equalizer Preprocessing:** Developed an in-memory pipeline utilizing grayscale conversion, border cropping, and Gaussian blur to systematically destroy spatial dataset leakage, such as format signatures and color biases, before feature extraction.
* **Dual-Stream CNN Architecture:** Engineered a parallel ResNet-50 framework that physically splits spatial and spectral information into different streams. A Gaussian-bottlenecked stream isolates macroscopic lesion morphology, while a Fast Fourier Transform (FFT)-magnitude stream targets periodic diffusion upsampling artifacts.
* **Robust Out-of-Distribution (OOD) Generalization:** Demonstrated that while the standard EfficientNet-B0 baseline suffers catastrophic domain collapse (AUC 0.5494) on cross-checkpoint unseen generators, SPECTRAFORGE maintains robust domain-invariant detection with an OOD AUC of 0.9277.
* **High-Precision Forensic Detection:** Attained a near-perfect Precision of 0.9931\0.0056 and an AUC of 0.9971\0.0016 on a strictly controlled 2,000-image clinical and synthetic dermoscopy cohort, ensuring minimal false positive quarantines in medical data ingestion pipelines.

<br>
<a href="getting ready" class="btn btn-sm btn-outline">Code & Resources</a>

<hr>

**Status:** Under Review at IEEE DSAA, 2026. **Authors:** A. Kumar, L. Chhetri, D. Das
