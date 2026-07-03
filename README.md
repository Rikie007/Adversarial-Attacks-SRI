# Adversarial Attacks – SRI Research Experiments

A structured study of adversarial robustness across multiple neural network architectures using **FGSM** (Fast Gradient Sign Method) and **PGD** (Projected Gradient Descent) attacks.

Conducted as part of a supervised research internship (SRI) under faculty guidance.

---

## Experiments Overview

### Experiments 1, 2, 3 — MNIST (Pixel, Rotation, Combined)
**Notebook:** `SRI_Experiment1,2,3_Pixel_Rotation_Combined.ipynb`

| Experiment | Attack Type | Target |
|---|---|---|
| 1 | Pixel-value perturbation (FGSM/PGD) | Custom CNN on MNIST |
| 2 | Rotation-based geometric attack | Custom CNN on MNIST |
| 3 | Combined (pixel + rotation) joint attack | Custom CNN on MNIST |

- Trains a baseline CNN on MNIST and evaluates clean accuracy
- Generates adversarial examples under varying epsilon (ε) budgets
- Compares single-step (FGSM) vs iterative (PGD) attack effectiveness
- Visualizes original vs perturbed images side-by-side

---

### Experiment 4 — Animal Image Classifier (ResNet-18)
**Notebook:** `SRI_Experiment4_Animal_Classification.ipynb`

- Fine-tunes a pretrained **ResNet-18** on an animal classification dataset
- Applies pixel-based FGSM/PGD white-box attacks
- Measures accuracy drop and visualizes misclassified adversarial samples

---

### Experiment 5 — Traffic Sign Classification (GTSRB)
**Notebook:** `SRI_Experniment5_VehicleSignClassification_Model_Attack.ipynb`

- Trains a CNN on the **GTSRB** (German Traffic Sign Recognition Benchmark) dataset
- Applies pixel-based adversarial perturbations
- Highlights safety-critical implications: a stop sign misclassified under imperceptible noise

---

## Tech Stack

| Tool | Purpose |
|---|---|
| Python | Core language |
| PyTorch | Model training & attack implementation |
| torchvision | Datasets (MNIST, GTSRB) & pretrained ResNet-18 |
| NumPy | Perturbation calculations |
| Matplotlib | Visualization of adversarial examples |

---

## Key Concepts

- **FGSM** — Single-step attack using the sign of the loss gradient w.r.t input
- **PGD** — Iterative FGSM with projection back into ε-ball; stronger attack
- **Epsilon (ε)** — Controls perturbation magnitude; imperceptible at low values
- **White-box attack** — Attacker has full access to model weights and gradients

---

## References

- Goodfellow et al. (2015) — *Explaining and Harnessing Adversarial Examples*
- Madry et al. (2018) — *Towards Deep Learning Models Resistant to Adversarial Attacks*
- ETH Zürich — *Reliable and Interpretable Artificial Intelligence*

---

## Guide

Supervised Research Internship — [Professor Name], [Institution]
