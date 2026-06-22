---
layout: page
title: Ashokan Brahmi Script OCR
description: Degraded stone inscription recognition via SimCLR, CRNN, and Morphological Domain Randomization.
img: assets/img/Brahmi.png
importance: 3
category: active research
---
<div class="row justify-content-sm-center">
  <div class="col-sm-12 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/Brahmi.png" title="Brahmi Preprocessing" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Original stone inscription degradation vs. morphological domain randomization preprocessing.
</div>

### The Data Scarcity Bottleneck
Ashokan Brahmi inscriptions are severely degraded by cracks, erosion, and weathering. Standard OCR fails because large, labeled datasets for ancient Indic scripts do not exist. We engineered a synthetic degradation pipeline to generate 150,000 sequence-level images using WGAN-GP.

### Self-Supervised Feature Extraction
To learn robust visual features from unlabeled, real-world stone inscriptions, we applied the SimCLR algorithm with a ResNet-34 backbone using NT-Xent contrastive loss. This extracts degradation-invariant representations without requiring human annotation.

### Morphological Domain Randomization (MDR)
A severe domain gap exists between GAN-generated strokes (thin, uniform) and authentic chiseled stone strokes (thick, irregular). We introduced MDR—dynamically applying heavy dilation and erosion during training. 
* **Impact:** Reduced the Character Error Rate (CER) on real inscription images from ~85% to 30-40%.

The final pipeline fuses the SimCLR-pretrained ResNet-34 encoder with a BiLSTM sequence modeler and CTC loss, successfully bypassing traditional character segmentation bottlenecks.
