# Notebooks

This directory contains the main Jupyter Notebook used for model comparison and customer segmentation analysis.

---

## File

- **model_comparison_analysis.ipynb**

---

## Overview

The notebook implements a complete machine learning workflow focused on:

- Comparing model families under controlled experimental design  
- Evaluating model performance using robust metrics  
- Analyzing trade-offs between performance and stability  
- Identifying meaningful customer segments through clustering  

---

## Contents

### 1. Data Exploration

- Initial inspection of dataset structure  
- Analysis of feature distributions  
- Identification of potential non-linear patterns  

---

### 2. Data Preprocessing

- Train-test split (70/30, stratified)  
- Feature scaling (applied only for SVM)  
- Preparation for modeling and cross-validation  

---

### 3. Model Training

Two model families are implemented:

- **Random Forest (Ensemble Method)**
- **Support Vector Machine (RBF Kernel)**

Controlled hyperparameter tuning:

- Random Forest → number of trees  
- SVM → regularization parameter (C)  

---

### 4. Model Evaluation

- Cross-validation (5-fold stratified)  
- Metrics:
  - F1-score  
  - Precision  
  - Recall  
  - Accuracy  
  - ROC-AUC  

- Comparison of:
  - Performance  
  - Stability (standard deviation across folds)  

---

### 5. Trade-Off Analysis

- Evaluation of performance vs stability  
- Interpretation of model behavior  
- Selection of best model based on business criteria  

---

### 6. Dimensionality Reduction

- PCA applied for visualization of customer behavior  
- Projection into 2D space for clustering interpretation  

---

### 7. Clustering Analysis

Two unsupervised methods are applied:

- **K-Means**
  - Determination of optimal number of clusters using silhouette score  
- **DBSCAN**
  - Analysis of density-based clusters and noise points  

---

### 8. Segmentation Insights

- Identification of customer segments:
  - Small retail buyers  
  - Large wholesale buyers  

- Interpretation of behavioral differences  
- Business implications of segmentation  

---

## Purpose

This notebook demonstrates a structured approach to:

- Model comparison and evaluation  
- Understanding trade-offs in machine learning  
- Combining supervised and unsupervised learning  
- Translating technical results into business insights  

---

## Notes

- All preprocessing steps are performed within the notebook  
- No data leakage is introduced during cross-validation  
- The workflow is designed to be reproducible and interpretable  
