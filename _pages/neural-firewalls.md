---
layout: page
title: "Intrinsic Neural Firewalls for Cyber-Physical Systems: Robust Anomaly Rejection via Deep Delta Residual Overwrites"
permalink: /publications/neural-firewalls/
---

### Abstract

Modern Industrial Cyber-Physical Systems heavily leverage Web 6.0 communication fabrics, thus creating a practical opportunity for False Data Injection Attacks (FDIA). The adversary generates statistically plausible measurements, misleading deep-learning-based intrusion detection. External detectors suffer from latencies, need pre-labeled attack data, and cannot prevent internal corruption of the state. This work proposes Deep Delta Learning Firewall (DDL-FW), an intrinsic defense architecture designed specifically for CPS, which is not dependent on any attack examples during training. While other defenses typically employ an additional detector, DDL-FW integrates the defense functionality directly in the residual connections, substituting a simple addition of the residual to the state vector with a depth-wise read-compare-write routine, based on the principles of Deep Delta Learning (DDL). This way, every transformer block obtains the ability to explicitly reject anomalous input instead of absorbing it. Training on clean sequences of observations, DDL-FW produces anomaly scores at zero overhead as a result of residual errors accumulation through layers. Four channels of the extended residual state ensure the quarantine of adversarial perturbation on layer borders and stop its propagation into the global memory stream. Experiments were conducted using the benchmark of HAI 21.03, including 79 sensors distributed between turbine, boiler, and water treatment systems. DDL-FW exhibits an F1 score of 0.7206 and a false positive rate of 2.01% compared to inferior results of Isolation Forest, One-Class SVM, and statistical baselines by large margins, being 1.3M parameters only.


### Key Methodologies & Contributions
* **Intrinsic Defense Architecture:** Proposed the Deep Delta Learning Firewall (DDL-FW), an internal defense mechanism for Cyber-Physical Systems that replaces standard additive residual connections with a depth-wise read-compare-write routine based on Deep Delta Learning principles.---
layout: page
title: "Intrinsic Neural Firewalls for Cyber-Physical Systems: Robust Anomaly Rejection via Deep Delta Residual Overwrites"
permalink: /publications/neural-firewalls/
---

### Abstract

Modern Industrial Cyber-Physical Systems heavily leverage Web 6.0 communication fabrics, thus creating a practical opportunity for False Data Injection Attacks (FDIA). The adversary generates statistically plausible measurements, misleading deep-learning-based intrusion detection. External detectors suffer from latencies, need pre-labeled attack data, and cannot prevent internal corruption of the state. This work proposes Deep Delta Learning Firewall (DDL-FW), an intrinsic defense architecture designed specifically for CPS, which is not dependent on any attack examples during training. While other defenses typically employ an additional detector, DDL-FW integrates the defense functionality directly in the residual connections, substituting a simple addition of the residual to the state vector with a depth-wise read-compare-write routine, based on the principles of Deep Delta Learning (DDL). This way, every transformer block obtains the ability to explicitly reject anomalous input instead of absorbing it. Training on clean sequences of observations, DDL-FW produces anomaly scores at zero overhead as a result of residual errors accumulation through layers. Four channels of the extended residual state ensure the quarantine of adversarial perturbation on layer borders and stop its propagation into the global memory stream. Experiments were conducted using the benchmark of HAI 21.03, including 79 sensors distributed between turbine, boiler, and water treatment systems. DDL-FW exhibits an F1 score of 0.7206 and a false positive rate of 2.01% compared to inferior results of Isolation Forest, One-Class SVM, and statistical baselines by large margins, being 1.3M parameters only.


### Key Methodologies & Contributions
* **Intrinsic Defense Architecture:** Proposed the Deep Delta Learning Firewall (DDL-FW), an internal defense mechanism for Cyber-Physical Systems that replaces standard additive residual connections with a depth-wise read-compare-write routine based on Deep Delta Learning principles.
* **Zero-Cost Anomaly Scoring:** Generated an intrinsic anomaly score ($\mathcal{A}=\sum_{l=1}^{L}||v_{l}^{\top}-k_{l}^{\top}X_{l}||_{2}$) as a free byproduct of the forward pass, utilizing accumulating residual errors without requiring external detection modules or additional computational latency.
* **Expanded-State Memory Quarantine:** Implemented a four-channel expanded memory state ($d_{v}=4$) that isolates adversarial perturbations at layer boundaries, preventing contamination from propagating into the global compute stream.
* **Attack-Agnostic Detection:** Demonstrated a zero-shot, attack-agnostic detection framework trained exclusively on clean sensor sequences, achieving an F1 score of 0.7206 and a 2.01% False Positive Rate on the HAI 21.03 benchmark with a lightweight 1.3M parameter footprint.

<br>
<a href="https://github.com/Latchan-Ch/Intrinsic-Neural-Firewalls" class="btn btn-outline">Code & Resources</a>

<hr>

**Status:** Accepted for Oral Presentation at WIN 6.0, 2026. **Authors:** R. Das, L. Chhetri, A. Kumar, P. Ghosal

* **Expanded-State Memory Quarantine:** Implemented a four-channel expanded memory state ($d_{v}=4$) that isolates adversarial perturbations at layer boundaries, preventing contamination from propagating into the global compute stream.
* **Attack-Agnostic Detection:** Demonstrated a zero-shot, attack-agnostic detection framework trained exclusively on clean sensor sequences, achieving an F1 score of 0.7206 and a 2.01% False Positive Rate on the HAI 21.03 benchmark with a lightweight 1.3M parameter footprint.

<br>
<a href="https://github.com/Latchan-Ch/Intrinsic-Neural-Firewalls" class="btn btn-outline">Code & Resources</a>

<hr>

**Status:** Accepted for Oral Presentation at WIN 6.0, 2026. **Authors:** R. Das, L. Chhetri, A. Kumar, P. Ghosal
