# Customer Behavior: Model Comparison & Segmentation Analysis

## Overview

This project analyzes customer behavioral data to compare machine learning model families and identify meaningful customer segments.

The objective is not only to build predictive models, but to evaluate how different modeling approaches perform under controlled conditions, and to understand the trade-offs between performance, stability, and business impact.

In addition, unsupervised learning techniques are applied to uncover latent customer segments based on purchasing behavior and engagement patterns.

---

## Objectives

- Compare two model families:
  - Ensemble methods (Random Forest)
  - Support Vector Machines (RBF Kernel)
- Evaluate model performance using robust metrics beyond accuracy
- Analyze trade-offs between model performance and stability
- Identify the most suitable model from a business perspective
- Apply clustering techniques to discover customer segments
- Generate actionable insights from both supervised and unsupervised learning

---

## Technologies Used

- Python (Pandas, NumPy, Scikit-learn)
- Machine Learning:
  - Random Forest
  - Support Vector Machine (SVM)
- Unsupervised Learning:
  - K-Means
  - DBSCAN
- Model Evaluation:
  - F1-score
  - ROC-AUC
  - Cross-validation
- Dimensionality Reduction:
  - PCA

---

## Experimental Design

- Train-test split: 70/30 with stratification  
- Cross-validation: 5-fold stratified CV  
- Primary selection metric: **F1-score**  
- Controlled tuning:
  - Random Forest → `n_estimators = [100, 300, 600]`
  - SVM (RBF) → `C = [0.1, 1, 10]`  

Preprocessing was adapted to each model:

- Random Forest → no scaling required  
- SVM → standardized features (to prevent scale sensitivity)  

All transformations were applied without data leakage.

---

## Model Performance

| Model            | Accuracy | Precision | Recall | F1-score | ROC-AUC |
|------------------|---------|----------|--------|---------|--------|
| Random Forest    | 0.81    | 0.79     | 0.79   | 0.79    | 0.88   |
| SVM (RBF Kernel) | 0.80    | 0.80     | 0.75   | 0.77    | 0.88   |

---

## Key Findings

### Model Comparison

- Random Forest achieved higher **F1-score** and **Recall**
- SVM showed slightly higher **Precision** and better **stability**
- Both models demonstrated similar **ROC-AUC**, indicating comparable class separation ability

### Trade-Off Analysis

- **Random Forest**
  - Better performance
  - Higher recall (fewer missed target customers)
  - Slightly less stable across folds  

- **SVM (RBF)**
  - More stable (lower variance)
  - Better precision (fewer false positives)
  - Slightly lower overall performance  

---

## Business Perspective

From a business standpoint, **false negatives are more costly** than false positives:

- Missing high-value customers → lost revenue opportunities  
- Misclassifying low-value customers → only increases operational cost  

Therefore, **Random Forest is selected for deployment** due to its higher recall and stronger overall performance.

---

## Customer Segmentation

Two clustering techniques were applied:

### K-Means

- Optimal clusters: **K = 2**
- Segments identified:
  - **Small Retail Buyers**
    - Low spending, infrequent purchases  
  - **Large Wholesale Buyers**
    - High spending, frequent purchases

<img width="925" height="790" alt="output" src="https://github.com/user-attachments/assets/30111df0-bc61-49da-a29d-c4a256721cf6" />


### DBSCAN

- Detected similar segments but with:
  - Higher sensitivity to parameters  
  - Presence of noise points  
  - Less stable clustering structure

<img width="565" height="455" alt="output2" src="https://github.com/user-attachments/assets/4b47a94f-72e9-4298-b6bb-13cc9e265844" />



---

## Segmentation Insights

- Clear distinction between low-value and high-value customers  
- High-value customers represent key revenue drivers  
- Low-value customers are ideal targets for promotions and engagement strategies  

---

## Key Insights

- Customer behavior is driven by **non-linear relationships**
- Ensemble models capture these patterns more effectively  
- Model selection should consider:
  - Performance metrics  
  - Stability  
  - Business cost of errors  
- Simple clustering can reveal **highly actionable customer segments**

---

## Conclusion

This project demonstrates the importance of:

- Comparing model families instead of relying on a single approach  
- Using appropriate evaluation metrics beyond accuracy  
- Understanding trade-offs between performance and stability  
- Integrating machine learning with business decision-making  

Random Forest provided the best balance between predictive power and business impact, while clustering revealed meaningful customer segments that can support targeted strategies.

---
