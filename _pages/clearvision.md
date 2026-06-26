---
layout: page
title: "ClearVision: A Physics-Informed Lightweight GAN for Real-Time Enhancement of Turbid Underwater Imagery"
permalink: /publications/clearvision/
---

### Abstract

Autonomous Underwater Vehicles (AUVs) operating in estuarine and benthic zones encounter severe visibility degradation due to the presence of heavy sediment suspension. Existing image enhancement models struggle to maintain a balance between image quality and processing speed, limiting their use in real-time underwater explorations. We introduce ClearVision, a lightweight GAN-based architecture specifically tailored for underwater turbid environments. The model incorporates physics-informed loss functions that approximate depth-dependent scattering and preserve color consistency, operating efficiently with only 9.1 million parameters. While achieving 50 Frames Per Second (FPS) on server hardware, the model is optimised for embedded AUV platforms. The model attains a Peak Signal-to-Noise Ratio (PSNR) of 19.18 dB, Structural Similarity (SSIM) of 0.726, and Underwater Image Quality Measure (UIQM) of 3.13. To evaluate its practical impact, we perform a downstream validation using ORB feature matching. ClearVision achieves a 234-fold increase in feature matching over raw turbid input, which averages just 1.75 matches, thereby enabling reliable robotic AUV navigation in sediment-degraded environments.


### Key Methodologies & Contributions
* **Physics-Informed Lightweight GAN:** Developed a lightweight Generative Adversarial Network (GAN) architecture specifically tailored for extremely turbid underwater environments, incorporating physics-informed loss functions that approximate depth-dependent light scattering.
* **Optimal Speed-Quality Trade-off:** Engineered an efficient architecture with only 9.1M parameters, capable of real-time processing at 50 FPS on NVIDIA T4 hardware, significantly outperforming high-parameter models like Sea-Pix GAN (54M parameters).
* **Extreme Turbidity Benchmarking:** Evaluated model robustness on a curated composite dataset of severely sediment-degraded imagery from Turbid-UIEB and Turbid-LSUI, moving beyond standard clear oceanic benchmarks.
* **Downstream Robotic Utility:** Validated real-world robotic utility by demonstrating a 234-fold increase in ORB feature matching correspondences over raw turbid input, directly enabling reliable Visual SLAM and navigation for Autonomous Underwater Vehicles (AUVs).

<br>
<a href="https://github.com/dishantroland2025/ClearVision-Turbidity-Resilient-GAN" class="btn btn-outline">Code & Resources</a>

<hr>

**Status:** Accepted for Oral Presentation at IEEE OCEANS Sanya, 2026. **Authors:** R. Singh, D. Das, A. Pradhan
