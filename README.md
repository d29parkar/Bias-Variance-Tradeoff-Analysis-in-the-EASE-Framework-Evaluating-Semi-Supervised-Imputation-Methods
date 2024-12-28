# Bias-Variance Tradeoff Analysis in the EASE Framework

## Overview
This project extends the **Efficient and Adaptive Semi-Supervised Estimator (EASE)** framework to incorporate **K-Nearest Neighbors (KNN)** and **Loess Regression** as imputation methods. It evaluates their performance in terms of bias, variance, and robustness under both linear and nonlinear modeling assumptions.

The repository contains simulation results, analysis scripts, and findings aimed at improving parameter estimation in semi-supervised learning settings where labeled data is scarce but unlabeled data is abundant.

## Key Concepts

### Semi-Supervised Learning (SSL)
- Labeled data is often limited and costly.
- Unlabeled data is abundant and can enhance parameter estimation.
- SSL aims to leverage unlabeled data for better model performance.

### EASE Framework
- A semi-supervised approach combining supervised (OLS) and semi-supervised estimators.
- Uses **semi-nonparametric (SNP) imputation** to predict outcomes for unlabeled data.
- Improves robustness and efficiency, especially under model misspecification.

---

## Objectives
1. **Extend EASE Framework**:
   - Add **KNN** and **Loess Regression** as imputation methods.
2. **Evaluate Performance**:
   - Compare bias and variance of imputation methods under various conditions:
     - Model correctness (linear vs. nonlinear relationships).
     - Predictor dimensionality (p = 2, p = 4).
     - Noise levels (σ² variations).
     - Ratio of labeled to unlabeled data (r = 5, r = 10).
3. **Provide Guidelines**:
   - Recommend methods based on data structure and modeling requirements.

---

## Imputation Methods
- **Kernel Smoothing (KS)** with Sliced Inverse Regression (SIR): Effective for dimensionality reduction.
- **Kernel Machine (KM) Regression**: Robust for both linear and nonlinear relationships.
- **K-Nearest Neighbors (KNN)**: Simple and efficient for linear relationships.
- **Loess Regression**: Flexible but less effective in high-dimensional settings.

---

## Results
- **Kernel Machine (KM)** achieved the lowest bias and variance across settings.
- **KNN** performed well under linear relationships.
- **Loess Regression** showed flexibility but struggled with high-dimensional and nonlinear data.
- **SIR + KS** was effective for dimensionality reduction but outperformed by KM and KNN.

---

## Repository Structure
- `data/`: Contains simulation datasets.
- `scripts/`: Includes R scripts for simulations and analysis.
- `results/`: Contains output files and visualizations of bias-variance tradeoff.
- `docs/`: Documentation and report files.
- `README.md`: This file.

---

