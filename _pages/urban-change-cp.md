---
layout: page
title: "Risk-Controlled Urban Change Detection: Conformal Prediction Wrappers for Provable Reliability in High-Resolution Satellite Imagery"
permalink: /publications/urban-change-cp/
---

### Abstract

Satellite-based urban change detection enables an emerging generation of geospatial intelligence applications, from disaster damage assessments to spatial expansion monitoring; however, the deep learning models powering these systems lack formal reliability metrics for individual predictions. Even a model achieving an impressive 89% aggregate F1-score can still be systematically wrong exactly in the regions where accuracy is most critical: building boundaries, shadow margins, and active construction sites. This paper introduces a rigorous statistical approach to transformer-based satellite change detection using Marginal Split Conformal Prediction (CP). Working on top of the pre-trained Bitemporal Image Transformer (BIT) and the well-established LEVIR-CD benchmark, we calibrate a non-conformity threshold on the validation split and generate pixel-wise prediction sets. This achieves distribution-free, statistically rigorous 1 − α coverage bounds without requiring any re-training of the model weights. Our optimized implementation attains F1 = 89.94% and IoU = 81.72% on the LEVIR-CD test set, outperforming all published baselines. Furthermore, conformal calibration reveals a novel structural property specific to geospatial transformers: BIT operates in a near-binary confidence regime where spatial ambiguity emerges as Empty Prediction Sets rather than dual-class uncertainty. This constitutes the first formal characterisation of confidence distribution structure in remote-sensing change detection.


### Key Methodologies & Contributions
* **Conformal Prediction Wrapper:** Deployed Marginal Split Conformal Prediction on top of the pre-trained Bitemporal Image Transformer (BIT) to generate distribution-free, statistically rigorous 1-α coverage bounds for individual pixel-level predictions without retraining model weights.
* **Optimized BIT Implementation:** Corrected a widespread normalization error in the BIT training pipeline to recover full network accuracy, leading to state-of-the-art performance of F1=89.94% and IoU=81.72% on the LEVIR-CD benchmark dataset.
* **Bimodal Confidence Characterization:** Exposed a previously undescribed bimodal confidence structure in geospatial transformers through conformal calibration, where spatial ambiguity in boundary zones and active construction sites emerges as Empty Prediction Sets (EPS) rather than dual-class uncertainty.
* **Operational Reliability Metrics:** Provided a formally justified, computationally lightweight system enabling automated flagging of geometrically ambiguous pixels (the 10% EPS tail) for human-in-the-loop disaster assessment and geospatial intelligence workflows.

<br>
<a href="https://github.com/HaloMind-Research/Conformal-Satellite-Change-Detection" class="btn btn-primary">Code & Resources</a>

<hr>

**Status:** Under Review at ICCI, 2026. **Authors:** A. Mukherjee, A. Kumar, S. Bala, S. R. Verma, A. Anand, H. Das, L. Chhetri
