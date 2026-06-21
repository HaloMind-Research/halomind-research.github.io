---
layout: page
title: DDL-Mamba 
description: Geometric Residual Learning for 3D Medical Image Segmentation.
importance: 4
category: active research
---

### Architectural Formulation
Dense 3D State Space Models inherently suffer from representation drift when processing complex volumetric data. To resolve this, we developed a novel Delta-Mamba framework that integrates Deep Delta Learning (DDL) blocks into a U-Mamba backbone, specifically targeting concentric cardiac structures.

### Geometric Manifold Stabilization
We engineered the DDL block with $L_2$-normalized weights to stabilize the geometric manifold across deep encoder layers. To enforce strictly non-negative global slot amplitudes, we apply a Softplus constraint:

$$\gamma = \text{Softplus}(W_{norm} \cdot x)$$

This formulation prevents the training instability typically observed in unconstrained routing mechanisms. 

### Layer-Wise Explainability
Unlike standard Transformers or prior Mamba-based architectures, which act as black boxes, our architecture implements $\beta$-gate visualization. This provides a geometrically interpretable, layer-wise explainability mechanism for every segmentation decision—a critical requirement for trustworthy medical AI deployments.
