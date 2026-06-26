---
layout: page
title: "Interpretable Solar Panel Defect Detection via Fuzzy Rule Extraction from Deep Learning Architectures"
permalink: /publications/solar-defect/
---

### Abstract

The reliability of solar energy infrastructure depends heavily on early detection of panel defects, yet most deep learning models remain opaque, which is a serious concern when operators must trust and act on automated decisions. Motivated by this gap, we propose a novel framework that automatically extracts human-readable fuzzy logic rules from trained convolutional and transformer-based classifiers, providing transparent defect severity predictions without any manual rule engineering. We evaluate our approach on the ELPV benchmark dataset of 2,624 electroluminescence images. Results show that modern hierarchical architectures, namely Swin Transformer and ConvNeXt, achieve substantially higher feature-to-severity correlations (0.78 to 0.82) compared to classical CNNs (0.64), yielding more reliable and consistent fuzzy inference rules. Our best model, SwinTiny, achieves 80.96% overall accuracy while simultaneously generating interpretable IF-THEN decision boundaries, directly bridging the gap between high-performing black-box models and the transparency standards demanded by real-world solar farm operations.


### Key Methodologies & Contributions
* **Automated Fuzzy Rule Extraction:** Proposed an end-to-end neuro-fuzzy framework that automatically extracts human-readable IF-THEN logic rules from trained convolutional and transformer-based classifiers without manual rule engineering.
* **Architectural Interpretability Benchmarking:** Demonstrated that modern hierarchical architectures (Swin Transformer, ConvNeXt) yield significantly higher feature-to-severity Pearson correlations (0.78 to 0.82) compared to classical CNNs like ResNet50 (0.64), leading to cleaner decision boundaries and more trustworthy fuzzy rules.
* **Graded Confidence Calibration:** Leveraged continuous fuzzy membership functions to produce graded confidence scores that naturally resolve the inherent classification ambiguity of borderline, mild-defect cases.
* **High-Performing Transparent Operations:** Achieved 80.96% overall accuracy with a Swin-Tiny backbone on the ELPV benchmark dataset while exposing interpretable decision logic and broad spatial attention mapping for critical solar farm maintenance decisions.

<br>
<a href="https://github.com/HaloMind-Research/Interpretable-Solar-Defect-Detection" class="btn btn-sm btn-outline">Code & Resources</a>

<hr>

**Status:** Under Review at ICCI, 2026. **Authors:** S. R. Verma, A. Kumar, A. Anand, H. Das, L. Chhetri
