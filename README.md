# 📊 Customer Churn Prediction – Flagship Project

## 1. Problem Statement
Customer churn is a major challenge for subscription-based businesses.  
The objective of this project is to predict customer churn and identify key drivers behind churn to enable proactive retention strategies.

---

## 2. Dataset Overview
**Source:** Customer Churn Dataset (Banking Domain)  
**Records:** 10,000 customers  
**Target Variable:** `Exited`  
- 1 → Churn  
- 0 → Retained  

### Key Features
- **Demographics:** Age, Gender, Geography  
- **Account Information:** Balance, CreditScore, NumOfProducts  
- **Customer Behavior:** IsActiveMember, Tenure  

---

## 3. Exploratory Data Analysis (EDA)
### Key Findings
- Germany shows the highest churn rate among regions.
- Churn increases significantly with age.
- Customers with zero balance churn more.
- Inactive members are strong churn indicators.
- Customers owning fewer products are more likely to churn.

---

## 4. Feature Engineering
- Removed identifier columns (`RowNumber`, `CustomerId`, `Surname`)
- One-hot encoded categorical variables
- Standardized numerical features
- Train-test split with stratification

---

## 5. Modeling & Evaluation
### Models Used
- Logistic Regression (Baseline)
- Logistic Regression (Class-weight Balanced)
- Decision Tree Classifier (Balanced)

### Best Model
**Decision Tree Classifier**
- Selected due to superior churn recall and highest ROC-AUC among tested models.
- `max_depth = 5`
- `class_weight = balanced`

### Performance Highlights
- ROC-AUC: **~0.84**
- Churn Recall: **~76%**
- Balanced trade-off between churn recall and model interpretability

---

### 6. Business Insight from Feature Importance

- Older customers are significantly more likely to churn.
- Customers with fewer products show higher churn risk.
- Inactive members are strong churn indicators.
- German customers show higher churn impact compared to other regions.

These insights can be directly used for targeted customer retention strategies.

---

## 7. Tools & Technologies
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- Jupyter Notebook

---

## 8. Conclusion
This project demonstrates an end-to-end churn prediction pipeline, combining data analysis, feature engineering, and machine learning to deliver actionable business insights.