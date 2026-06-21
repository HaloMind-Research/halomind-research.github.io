---
layout: page
title: Ionospheric TEC Forecasting (CNN-DDL)
description: Zero-shot cross-solar-cycle generalization using Deep Delta Learning and Conformal Prediction.
importance: 1
category: active research
---

### Theoretical Formulation
[cite_start]Accurate forecasting of ionospheric Total Electron Content (TEC) during severe geomagnetic storms is critical for maintaining GNSS integrity[cite: 560]. [cite_start]Standard sequential models suffer from chronological overfitting, memorizing epoch-specific plasma backgrounds[cite: 584, 586]. 

[cite_start]To solve this, we architected the Convolutional Neural Network with Deep Delta Learning (CNN-DDL)[cite: 562]. [cite_start]Instead of predicting absolute TEC, the model learns the perturbation delta over a physical persistence baseline[cite: 590]:

$$\hat{T}_{t+1} = T_{t} + \hat{\Delta}_{t}$$

### The Dynamic Beta-Gate
[cite_start]We replaced standard additive Transformer residuals with an adaptive rank-1 update[cite: 843]. [cite_start]A dynamic gate ($\beta$) conditions the magnitude of the predicted correction on real-time solar wind variables[cite: 592]:

$$\beta = \sigma(W_{\beta}^{(2)}ReLU(W_{\beta}^{(1)}x))$$

[cite_start]This allows the network to amplify corrections during active conditions ($K_p \ge 5$) while suppressing noise during quiet periods[cite: 564]. 

### Zero-Shot Cross-Cycle Evaluation
[cite_start]Trained exclusively on the extreme May 2024 superstorm (Solar Cycle 25), the model was evaluated zero-shot on the March 2015 and September 2017 storms (Solar Cycle 24)[cite: 565]. 
* [cite_start]**Performance:** Achieved SOTA storm-time RMSE of 2.30 TECU (May 2024), outperforming BiLSTM, GRU, and SpatioTemporal ConvLSTM[cite: 565, 566].
* [cite_start]**Uncertainty Quantification:** Integrated Marginal Split Conformal Prediction, providing a mathematically guaranteed 90% empirical coverage bound[cite: 549].
