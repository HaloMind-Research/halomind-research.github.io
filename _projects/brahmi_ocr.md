---
layout: page
title: Ashokan Brahmi Script OCR
description: Degraded stone inscription recognition via SimCLR, CRNN, and Morphological Domain Randomization.
img: assets/img/brahmi_pipeline.png
importance: 3
category: active research
---

### The Data Scarcity Bottleneck
[cite_start]Ashokan Brahmi inscriptions are severely degraded by cracks, erosion, and weathering[cite: 284]. [cite_start]Standard OCR fails because large, labeled datasets for ancient Indic scripts do not exist[cite: 308]. [cite_start]We engineered a synthetic degradation pipeline to generate 150,000 sequence-level images using WGAN-GP[cite: 340].

### Self-Supervised Feature Extraction
[cite_start]To learn robust visual features from unlabeled, real-world stone inscriptions, we applied the SimCLR algorithm with a ResNet-34 backbone using NT-Xent contrastive loss[cite: 343, 445, 447]. [cite_start]This extracts degradation-invariant representations without requiring human annotation[cite: 454].

### Morphological Domain Randomization (MDR)
[cite_start]A severe domain gap exists between GAN-generated strokes (thin, uniform) and authentic chiseled stone strokes (thick, irregular)[cite: 416, 417]. [cite_start]We introduced MDR—dynamically applying heavy dilation and erosion during training[cite: 418, 419]. 
* [cite_start]**Impact:** Reduced the Character Error Rate (CER) on real inscription images from ~85% to 30-40%[cite: 423].

[cite_start]The final pipeline fuses the SimCLR-pretrained ResNet-34 encoder with a BiLSTM sequence modeler and CTC loss [cite: 346][cite_start], successfully bypassing traditional character segmentation bottlenecks[cite: 474].
