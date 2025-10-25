# 📈 VEESA Pipeline Demo (Functional Data Analysis with Explainable AI)

This repository is a **step-by-step demonstration** of the **VEESA pipeline** — an Explainable AI framework for *Functional Data Analysis (FDA)* using **joint functional PCA (jfPCA)** and interpretable models such as **Random Forest**.

![R](https://img.shields.io/badge/R-4.3.2-blue?logo=r)

> 📄 Reference: [VEESA: Variability Extraction and Explainable Shape Analysis (Goode et al., 2025)](https://arxiv.org/abs/2501.07602)  
> 🧩 Original GitHub: [sandialabs/veesa](https://github.com/sandialabs/veesa)

---

## ⚙️ Project Overview

This project demonstrates how to:

1. **Load or simulate functional data** (e.g. spectroscopy curves).  
2. **Smooth and align functional data** using the *Square-Root Velocity Function (SRVF)* framework.  
3. **Apply joint functional PCA (jfPCA)** to extract **phase** and **amplitude** variability.  
4. **Train interpretable machine learning models**: Random Forest    
5. **Compute Permutation Feature Importance (PFI)** and visualize **principal direction functions (efPCs)**.

---

## 🧩 Notebook Workflow

| Step | File | Description |
|------|------|-------------|
| . | `set_up.ipynb` | Set up for full Veesa pepline (GridSearchCV) |
| 0 | `step_0.ipynb` | Data preparation / simulation |
| 1 | `step_1.ipynb` | Smoothing + SRVF alignment |
| 2+3 | `step_2+3.ipynb` | Functional PCA (jfPCA) and score extraction |
| 4+5+6 | `step_4+5+6.ipynb` | Random Forest + PFI + efPC visualization |
| Improvement | `step_bonus.ipynb` | Stability selection + tie-break + cumulation for PFI |

> 🔁 **Recommended:** Run in **Jupyter Notebook with R kernel** for full reproducibility and visualization.

---

## 🧭 Core Libraries

| Purpose | Packages |
|---------|----------|
| Functional Data Analysis | `veesa`, `fdasrvf`, `dplyr`, `tidyr`, `purrr` |
| Machine Learning | `randomForest` |
| Visualization | `ggplot2`, `patchwork`, `cowplot` |
| Utilities | `readr`, `stringr`, `reticulate` |

---

## 📊 Results & Insights

- 🌲 **Random Forest** is trained on **efPC scores** from jfPCA.  
- 🧠 **K-fold Cross Validation** is used to evaluate model accuracy/log-loss.  
- 🔍 **Permutation Feature Importance (PFI)** identifies which efPCs contribute most to the model.  
- 🌀 **Principal Direction plots (efPC)** show how each component affects the functional curves.  
- 🎯 Outputs include:  
  - Accuracy / Log-loss (or NMSE, R² if regression)  
  - Top-ranked efPCs by PFI  
  - Visualizations of functional variability

---


