# Data

This directory contains the dataset used for customer behavior analysis, model comparison, and segmentation.

---

## Dataset Description

The dataset includes customer behavioral and transactional features used to analyze purchasing patterns and classify customers into different channels.

Typical features include:

- Spending across product categories
- Purchase frequency
- Order size and intensity
- Customer engagement indicators

The target variable:

- **Channel** → Binary classification variable representing customer type or segment

---

## Purpose

This dataset is used for:

- Supervised learning:
  - Classification using Random Forest and SVM
- Unsupervised learning:
  - Customer segmentation using K-Means and DBSCAN
- Dimensionality reduction:
  - PCA for visualization of clusters

---

## Notes

- The dataset is used as the base input for all analysis and modeling steps  
- Preprocessing (scaling, transformations) is performed within the notebook  
- No modifications are made directly to this file to preserve data integrity and reproducibility  
