---
layout: page
title: "Benchmarking GAN Architectures for Underwater Imaging: The Trade-off Between Model Compactness and Real-Time Latency"
permalink: /publications/underwater-gan-analysis/
---

### Abstract

Underwater imaging suffers from severe degradation due to light absorption and scattering, complicating marine research and autonomous navigation. This study compares two GAN-based approaches, Sea-Pix-GAN and MuLA-GAN, for underwater image enhancement. Sea-Pix-GAN employs a wide U-Net architecture with high-weight L1 loss, while MuLA-GAN uses a narrow attention-based U-Net with VGG perceptual loss. Trained on four benchmark datasets, Sea-Pix-GAN achieves superior structural and perceptual quality with 54.42M parameters and 18.20 GFLOPs computational complexity. MuLA-GAN with 16.56M parameters and 13.10 GFLOPs reduces the model size by 70% but sacrifices perceptual quality. On T4 GPU, we demonstrate a trade-off between model size and latency: while MULA-GAN requires 70% fewer parameters, it incurs a 32% higher inference latency due to attention overhead. Our findings recommend Sea-Pix-GAN for latency-critical AUV navigation and MuLA-GAN for storage-constrained edge devices.

### Key Methodologies & Contributions
* **Rigorous GAN Architecture Benchmark:** Conducted a comprehensive evaluation comparing a wide U-Net with heavy reconstruction constraints against a compact, attention-guided residual network across four diverse datasets (LSUI, UIEB, UFO-120, and GoPro)[cite: 5].
* **The Attention Latency Paradox:** Uncovered a critical deployment trade-off demonstrating that despite a 70% reduction in parameter count (16.56M vs. 54.42M) and lower theoretical complexity (13.10 GFLOPs), attention mechanisms introduce significant global pooling and matrix synchronization overhead, resulting in a 32% increase in real-world GPU inference latency (9.46 ms vs. 7.15 ms)[cite: 5].
* **Structural and Perceptual Integrity Optimization:** Validated that high-weight $L_1$ loss ($\lambda=100$) yields a 16.33% higher average SSIM (0.9534 vs. 0.8196) and 61.89% higher average UIQM scores, successfully suppressing local artifacts and non-uniform color casts where semantic perceptual losses compromise fine structure[cite: 5].
* **Hardware-Targeted Deployment Framework:** Established clean optimization baselines proving Sea-Pix-GAN's pure convolutional execution is ideal for high-throughput streaming feeds (139.95 FPS) like real-time visual odometry, whereas MuLA-GAN remains highly optimal for ROM-constrained embedded systems[cite: 5].

<br>
<a href="https://github.com/dishantroland2025/Underwater-GAN-Analysis" class="btn btn-outline">Code & Resources</a>

<hr>

**Status:** Accepted at IEEE GCON, 2026. **Authors:** D. Das, R. Singh, A. Pradhan, P. Ghosal
