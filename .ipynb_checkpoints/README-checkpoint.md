# 📈 Veesa Pipeline Demo (Functional Data Analysis with Explainable AI)

This repository is a **step-by-step demonstration** of the **VEESA pipeline** — a modern Explainable AI framework for *functional data analysis (FDA)* using **joint functional PCA (jfPCA)** and interpretable models such as **Random Forest** and **Neural Network**.

![R](https://img.shields.io/badge/R-4.3.2-blue?logo=r)

> 📄 Reference: [VEESA: Variability Extraction and Explainable Shape Analysis (Goode et al., 2025)](https://arxiv.org/abs/2501.07602)  
> 🧩 Original GitHub: [sandialabs/veesa](https://github.com/sandialabs/veesa)

---

## ⚙️ Project Overview

The project demonstrates how to:
1. **Simulate or import functional data** (e.g., spectroscopy, temporal signals).  
2. **Perform smoothing** and **alignment** using *Square-Root Velocity Function (SRVF)* representation.  
3. **Apply joint functional PCA (jfPCA)** to extract *amplitude* and *phase* variability.  
4. **Train interpretable ML models**:
   - 🌲 Random Forest  
   - 🧠 Neural Network (Keras3 / TensorFlow backend)
5. **Compute feature importance (PFI)** and visualize **principal directions (efPCs)**.

---

## 🧩 Notebook Workflow

| Step | File | Description |
|------|------|-------------|
| 0 | `step_0.ipynb` | Data preparation and simulation setup |
| 1 | `step_1.ipynb` | Smoothing and alignment using SRVF |
| 2+3 | `step_2+3.ipynb` | Functional PCA (jfPCA) and feature extraction |
| 4 (1) | `step_4 (1).ipynb` | Random Forest model training |
| 4 (2) | `step_4 (2).ipynb` | Neural Network model training |
| 5+6 (1) | `step_5+6 (1).ipynb` | PFI + efPC visualization (Random Forest branch) |
| 5+6 (2) | `step_5+6 (2).ipynb` | PFI + efPC visualization (Neural Network branch) |

> 🔁 **Recommendation:** Run this project in **Jupyter Notebook (R kernel)** for the best reproducibility and visualization experience.

---

## 🧭 Core Libraries

| Category | Packages |
|-----------|-----------|
| **Functional Data Analysis** | `veesa`, `fdasrvf`, `tidyr`, `dplyr`, `purrr` |
| **Visualization** | `ggplot2`, `cowplot`, `patchwork` |
| **Machine Learning** | `randomForest`, `neuralnet`, `keras3`, `tensorflow` |
| **Pipeline & Utilities** | `reticulate`, `readr`, `base`, `stringr` |

---

## 📊 Results & Insights

- 🌲 **Random Forest** and 🧠 **Neural Network** both perform regression on the **functional coefficients (jfPCs)**.  
- 🔍 **Permutation Feature Importance (PFI)** reveals the most influential principal components.  
- 🌀 **Principal Direction (efPC)** plots illustrate how each component deforms the functional curves.  
- 🎯 Outputs include **NMSE**, **R²**, and **Top-15 efPCs** for each model.


