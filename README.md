📊 Customer Churn Prediction – Flagship Project
1. Problem Statement

Customer churn is a major challenge for subscription-based businesses.
The objective of this project is to predict customer churn and identify key drivers behind churn to enable proactive retention strategies.

2. Dataset Overview

Source: Customer Churn Dataset (Banking Domain)

Records: 10,000 customers

Target Variable: Exited (1 = Churn, 0 = Retained)

Key features include:

Demographics (Age, Gender, Geography)

Account information (Balance, CreditScore, NumOfProducts)

Customer behavior (IsActiveMember, Tenure)

3. Exploratory Data Analysis (EDA)

Key findings:

Germany shows the highest churn rate among regions.

Churn increases significantly with age.

Customers with zero balance and inactive members churn more.

Customers owning fewer products are more likely to churn.

EDA helped guide feature engineering and model selection.

4. Feature Engineering

Steps performed:

Removed identifier columns (RowNumber, CustomerId, Surname)

One-hot encoded categorical variables (Geography, Gender)

Standardized numerical features

Stratified train-test split to handle class imbalance

5. Models Tried
Logistic Regression (Baseline)

High overall accuracy

Poor recall for churn class

Logistic Regression (Class-Weighted)

Improved churn recall

Slightly reduced accuracy

Decision Tree (Final Model)

Class weight = balanced

Max depth = 5

Best trade-off between recall and ROC-AUC

6. Final Model Performance (Decision Tree)

Accuracy: ~77%

Churn Recall: ~76%

ROC-AUC: ~0.84

This model is well-suited for customer retention scenarios where identifying churners is more important than raw accuracy.

7. Feature Importance Insights

Top churn drivers:

Age

Number of Products

Active Membership Status

Account Balance

Geography (Germany)

These features provide actionable insights for targeted retention strategies.

8. Business Impact

Enables early identification of high-risk customers

Supports personalized retention campaigns

Helps businesses reduce churn-related revenue loss

9. Tech Stack

Python

Pandas, NumPy

Matplotlib, Seaborn

Scikit-learn
