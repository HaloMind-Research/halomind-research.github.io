---
layout: page
title: Ionospheric TEC Forecasting (CNN-DDL)
description: Zero-shot cross-solar-cycle generalization using Deep Delta Learning and Conformal Prediction.
img: assets/img/tec_forecasting.png
importance: 1
category: active research
---
<div class="row justify-content-sm-center">
  <div class="col-sm-12 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/tec_forecasting.png" title="TEC RMSE Heatmap" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Global Spatial RMSE Distribution during the May 2024 Superstorm.
</div>

### Theoretical Formulation
Accurate forecasting of ionospheric Total Electron Content (TEC) during severe geomagnetic storms is critical for maintaining GNSS integrity. Standard sequential models suffer from chronological overfitting, memorizing epoch-specific plasma backgrounds. 

To solve this, we architected the Convolutional Neural Network with Deep Delta Learning (CNN-DDL). Instead of predicting absolute TEC, the model learns the perturbation delta over a physical persistence baseline:

$$\hat{T}_{t+1} = T_{t} + \hat{\Delta}_{t}$$

### The Dynamic Beta-Gate
We replaced standard additive Transformer residuals with an adaptive rank-1 update. A dynamic gate ($\beta$) conditions the magnitude of the predicted correction on real-time solar wind variables:

$$\beta = \sigma(W_{\beta}^{(2)}ReLU(W_{\beta}^{(1)}x))$$

This allows the network to amplify corrections during active conditions ($K_p \ge 5$) while suppressing noise during quiet periods. 

### Zero-Shot Cross-Cycle Evaluation
Trained exclusively on the extreme May 2024 superstorm (Solar Cycle 25), the model was evaluated zero-shot on the March 2015 and September 2017 storms (Solar Cycle 24). 
* **Performance:** Achieved SOTA storm-time RMSE of 2.30 TECU (May 2024), outperforming BiLSTM, GRU, and SpatioTemporal ConvLSTM.
* **Uncertainty Quantification:** Integrated Marginal Split Conformal Prediction, providing a mathematically guaranteed 90% empirical coverage bound.
