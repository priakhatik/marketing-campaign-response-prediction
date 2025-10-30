# 🎯 Marketing Campaign Response Prediction Using Machine Learning

## Overview
This project evaluates machine learning models to predict customer responses in a marketing campaign. Using **Logistic Regression** and **K-Nearest Neighbors (KNN)**, the analysis focuses on model performance, emphasizing the importance of minimizing **False Negatives (FNs)**—customers who would have responded but were not targeted. The objective is to help businesses optimize marketing strategies and improve campaign ROI through data-driven insights.

---

## Objectives
- Predict customer response likelihood based on demographic and campaign-related data.  
- Compare performance between **Logistic Regression** and **KNN** models.  
- Evaluate models using key classification metrics—**Precision**, **Recall**, **F1-score**, and **Accuracy**.  
- Visualize performance through **Confusion Matrix**, **Precision-Recall Curve**, and **ROC Curve**.  
- Understand the business impact of False Positives (FPs) vs. False Negatives (FNs).  

---

## Data
- **Dataset Name:** Marketing Campaign Response Dataset  
- **Source:** Academic dataset provided for model evaluation and business analytics coursework.  
- **Records:** ~10,000 (varies based on preprocessing)  
- **Target Variable:** `Response` (binary: `1` = will respond, `0` = will not respond)

**Key Features**
- `Age`, `Income`, `Education`, `Marital_Status`, `Campaign_Contacts`, `Previous_Response`  
- Each attribute reflects demographic or behavioral information relevant to campaign targeting.

---

## Tools & Technologies
- Python (3.10+)  
- Pandas, NumPy  
- scikit-learn  
- Matplotlib, Seaborn  
- Jupyter Notebook  

---

## Methodology

### 1. Data Preprocessing
- Cleaned missing and inconsistent entries.  
- Encoded categorical variables using One-Hot Encoding.  
- Normalized numerical features for KNN performance.  
- Split data into 80% training and 20% testing sets.  

### 2. Model Training
- **Logistic Regression:** Baseline interpretable classifier.  
- **K-Nearest Neighbors (KNN):** Non-parametric model for performance comparison.  

### 3. Model Evaluation
For each model:
- Generated **Confusion Matrix** to interpret predictions.  
- Computed **Accuracy**, **Precision**, **Recall**, and **F1-Score**.  
- Plotted **Precision-Recall Curve** and **ROC Curve** with **AUC**.  
- Tested multiple classification thresholds (0.4, 0.5, 0.6) to observe impact on **Recall**.

---

## Results
| Model | Accuracy | Precision | Recall | F1-Score | AUC |
|--------|-----------|------------|----------|-----------|------|
| Logistic Regression | 83% | 81% | **87%** | 84% | 0.89 |
| KNN | 80% | 82% | 79% | 80% | 0.86 |

**Best Model:** Logistic Regression (higher recall and AUC)  
**Business Interpretation:**  
Reducing **False Negatives (FNs)** is crucial since missing potential customers leads to higher loss than targeting uninterested ones.

**Example Visualization:**  
![Model Evaluation – Precision Recall Curve](images/marketing_pr_curve.png)

---

## Key Insights
- Logistic Regression achieved better **Recall**, aligning with business objectives.  
- False Negatives were significantly reduced through threshold tuning.  
- Model explainability helped interpret which factors most influence customer response.  
- Campaign optimization should prioritize customers with higher predicted probabilities.

---

## Real-World Applications
- Customer targeting in direct and email marketing.  
- Campaign optimization and budget allocation.  
- Predictive analytics for lead scoring and retention modeling.  

---

## Future Work
- Incorporate more customer engagement variables (e.g., social or digital activity).  
- Apply advanced ensemble models (XGBoost, Random Forest).  
- Build an interactive dashboard for campaign response simulation.  
- Implement cost-sensitive learning to handle FN penalties explicitly.  

---

## Author
**Pria Khatik**  
M.S. in Artificial Intelligence & Business Analytics, University of South Florida  
🔗 [LinkedIn](https://www.linkedin.com/in/priyakhatik/)  
💬 *"In marketing, the cost of missing a willing customer is higher than reaching an uninterested one."*  

---
