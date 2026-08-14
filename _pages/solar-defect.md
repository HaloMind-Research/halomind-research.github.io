---
layout: page
title: "Interpretable Solar Panel Defect Detection via Fuzzy Rule Extraction from Hierarchical Vision Models"
permalink: /publications/solar-defect/
---

### Abstract

The reliability of the solar energy systems depends on the timely discovery of faults in panels; however, the lack of interpretability of most deep learning models can pose difficulties for users who have to trust and utilize the outcomes of automated systems. To overcome this problem, we present a new approach that automatically obtains human-understandable fuzzy rules from the latent features of trained transformers and CNN-based classification algorithms, thus providing interpretable predictions regarding the severity of defects without having to develop any explicit rules manually. The proposed methodology is tested using the ELPV benchmark dataset comprising 2,624 electroluminescence images. Experimental evidence suggests that modern hierarchical models, namely the Swin Transformer and ConvNeXt models, demonstrate significantly stronger correlation between features and severity (0.78-0.82) compared to traditional CNNs (0.64) and, therefore, can generate more reliable and consistent rules. The best performing model, namely Swin-Tiny, attains an overall accuracy of 80.96%, while simultaneously generating interpretable IF-THEN decision rules, and thus overcoming the gap between high-performance black-box models and the strict transparency standards required by real-world solar farm operations


### Key Methodologies & Contributions
* **Automated Fuzzy Rule Extraction:** Proposed an end-to-end neuro-fuzzy framework that automatically extracts human-readable IF-THEN logic rules from trained convolutional and transformer-based classifiers without manual rule engineering.
* **Architectural Interpretability Benchmarking:** Demonstrated that modern hierarchical architectures (Swin Transformer, ConvNeXt) yield significantly higher feature-to-severity Pearson correlations (0.78 to 0.82) compared to classical CNNs like ResNet50 (0.64), leading to cleaner decision boundaries and more trustworthy fuzzy rules.
* **Graded Confidence Calibration:** Leveraged continuous fuzzy membership functions to produce graded confidence scores that naturally resolve the inherent classification ambiguity of borderline, mild-defect cases.
* **High-Performing Transparent Operations:** Achieved 80.96% overall accuracy with a Swin-Tiny backbone on the ELPV benchmark dataset while exposing interpretable decision logic and broad spatial attention mapping for critical solar farm maintenance decisions.

<br>
<a href="https://github.com/HaloMind-Research/Interpretable-Solar-Defect-Detection" class="btn btn-outline">Code & Resources</a>

<hr>

**Status:** Under Review at ICVGIP, 2026. **Authors:** L. Chhetri, A. Kumar, D. Das, P. Ghosal
