---
layout: page
title: "Beyond Limited Labels: Safe Semi-Supervised Learning for Malaria Diagnosis"
permalink: /publications/malaria-ssl/
---

### Abstract

Deploying AI-based diagnostic tools in resource-constrained healthcare settings remains a critical challenge, where the scarcity of annotated medical images limits the viability of fully supervised approaches. Semi-supervised learning (SSL) offers a promising path forward, yet existing SSL methods trade deployment safety for annotation efficiency—relying on fixed confidence thresholds that produce dangerously overconfident errors in clinical settings where expert oversight is minimal. We address this gap with an uncertainty-guided SSL framework that integrates Monte Carlo dropout-based epistemic uncertainty estimation with adaptive confidence weighting, enabling safe pseudo-label filtering without sacrificing learning efficiency. Evaluated on malaria cell classification under low-resource conditions (20% labeled data), our method achieves a statistically significant 29.2% reduction in silent failure rate over the strongest SSL baseline (from 2.50% to 1.77%, paired t-test p = 0.0137, N = 6 seeds), while maintaining comparable diagnostic accuracy with 80% fewer labeled samples. Unlike standard SSL methods whose safety degrades sharply with threshold relaxation, our approach maintains consistent robustness across all operating points—a property essential for real-world deployment across diverse clinical environments.


### Key Methodologies & Contributions
* **Uncertainty-Guided SSL Framework:** Integrated Monte Carlo dropout-based epistemic uncertainty estimation with semi-supervised learning to provide a two-layer safety mechanism for pseudo-label generation.
* **Adaptive Confidence Weighting:** Replaced binary hard thresholding with soft confidence weighting to enable the gradual incorporation of mid-confidence predictions, maximizing annotation efficiency in low-resource environments.
* **Deployment Safety Improvement:** Achieved a statistically significant 29.2% relative reduction in the silent failure rate (from 2.50% to 1.77%, paired t-test p=0.0137) compared to the strongest tuned SSL baseline.
* **Clinical Robustness:** Maintained consistent diagnostic safety and robustness across relaxed confidence thresholds, overcoming the brittleness of standard semi-supervised methods while retaining high accuracy utilizing 80% fewer labeled samples.

<br>
<a href="https://github.com/HaloMind-Research/SafeMed-SSL" class="btn btn-outline">Code & Resources</a>

<hr>

**Status:** Under Review at IEEE DSAA, 2026. **Authors:** L. Chhetri, A. Kumar
