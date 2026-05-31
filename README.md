# Fintech Customer Risk & Behaviour Intelligence

## Customer Segmentation, Churn Prediction & Credit Behaviour Analytics

### Project Overview

Customer retention is one of the most critical challenges in the Banking, Financial Services, and Insurance (BFSI) sector. Losing customers directly impacts revenue, increases acquisition costs, and reduces long-term profitability.

This project analyzes customer behavior using the Bank Churners dataset and applies machine learning, statistical testing, and customer segmentation techniques to:

* Identify customers likely to churn
* Discover distinct customer segments
* Predict customer credit behavior
* Understand key drivers of churn
* Generate actionable business recommendations

The project follows a complete analytics workflow from Exploratory Data Analysis (EDA) to predictive modeling and business strategy formulation.

---

## Business Problem

Banks often struggle to identify customers who are likely to leave before churn actually occurs.

This project aims to answer the following business questions:

1. Which customers are at the highest risk of churn?
2. What behavioral patterns differentiate churned customers from retained customers?
3. Can customers be segmented into meaningful business groups?
4. Which factors contribute most to customer attrition?
5. How can the bank proactively reduce churn and increase customer lifetime value?

---

## Dataset Information

**Dataset:** Bank Churners (Credit Card Customers)

**Source:** Kaggle – Bank Churners Dataset by Sakshi Goyal

### Dataset Statistics

| Metric             | Value  |
| ------------------ | ------ |
| Total Customers    | 10,127 |
| Existing Customers | 8,500  |
| Attrited Customers | 1,627  |
| Churn Rate         | 16.07% |
| Features           | 23     |

### Key Variables

* Customer Age
* Gender
* Education Level
* Marital Status
* Income Category
* Credit Limit
* Revolving Balance
* Total Transaction Amount
* Total Transaction Count
* Utilization Ratio
* Months Inactive
* Customer Churn Status

---

## Project Workflow

### 1. Exploratory Data Analysis (EDA)

Performed:

* Missing value analysis
* Churn distribution analysis
* Feature distribution analysis
* Correlation analysis
* Outlier detection

Key Finding:

* Dataset contained no missing values.
* Customer churn rate was 16.07%.
* Transaction-related variables showed strong relationships with churn behavior.

---

### 2. Data Preprocessing

Performed:

* Label Encoding
* Feature Scaling using StandardScaler
* Feature Selection
* Train-Test Split

Purpose:

To prepare the dataset for clustering and machine learning algorithms.

---

### 3. Customer Segmentation

Technique Used:

**K-Means Clustering**

Methods:

* Elbow Method
* Silhouette Analysis

Final Clusters:

**K = 4**

### Segment Summary

#### Cluster 0 – Loyal Everyday Customers

* Moderate spending
* Consistent activity
* Stable engagement

#### Cluster 1 – Low Engagement Customers

* Low utilization
* Low activity
* Potential churn risk

#### Cluster 2 – Premium Credit Customers

* Very high credit limits
* High financial capacity
* Premium product opportunities

#### Cluster 3 – High Value Power Users

* Highest transaction activity
* Highest profitability
* Strategic retention segment

---

### 4. Churn Prediction

Three machine learning models were developed and compared.

| Model               | ROC-AUC Score |
| ------------------- | ------------- |
| Logistic Regression | 0.9079        |
| Random Forest       | 0.9880        |
| XGBoost             | 0.9921        |

### Best Model

**XGBoost**

ROC-AUC Score: **0.9921**

Reason:

XGBoost effectively captured complex customer behavior patterns and delivered the highest predictive performance.

---

### 5. Feature Importance Analysis

Top Churn Drivers:

1. Total Transaction Amount
2. Total Transaction Count
3. Total Count Change (Q4-Q1)
4. Total Revolving Balance
5. Total Relationship Count

### Business Insight

Customers exhibiting declining transaction activity are significantly more likely to churn.

---

### 6. Credit Behaviour Prediction

Regression Models Used:

* Linear Regression
* Ridge Regression
* Lasso Regression

Objective:

Estimate customer credit limits using behavioral and financial variables.

Business Value:

Supports credit risk management and customer credit strategy decisions.

---

### 7. Hypothesis Testing

#### Test 1: Income Category vs Churn

Statistical Test:

Chi-Square Test of Independence

Result:

* p-value = 0.0250

Conclusion:

Income category significantly influences customer churn behavior.

---

#### Test 2: Transaction Amount vs Churn

Statistical Test:

Mann-Whitney U Test

Result:

* p-value = 2.719 × 10⁻¹¹²

Conclusion:

Transaction behavior differs significantly between churned and retained customers.

---

## Key Business Insights

### Customer Retention

Customers with declining transaction amounts and lower engagement are more likely to churn.

### Revenue Protection

High-value customers contribute disproportionately to transaction volume and should be prioritized for retention programs.

### Customer Segmentation

Four distinct customer groups were identified, enabling personalized marketing and customer engagement strategies.

### Risk Monitoring

Transaction behavior serves as the strongest early-warning indicator for customer churn.

---

## Business Recommendations

### Recommendation 1: Churn Prevention Program

Target:

Low Engagement Customers

Actions:

* Cashback offers
* Personalized campaigns
* Fee waivers

---

### Recommendation 2: Premium Customer Upselling

Target:

Premium Credit Customers

Actions:

* Premium credit cards
* Wealth management products
* Exclusive banking services

---

### Recommendation 3: Protect High Value Customers

Target:

High Value Power Users

Actions:

* Loyalty rewards
* Dedicated relationship managers
* Exclusive customer benefits

---

### Recommendation 4: Early Warning Churn Monitoring

Track:

* Transaction Amount
* Transaction Count
* Relationship Count

These variables provide the strongest predictive signals for customer churn.

---

## Technologies Used

### Programming

* Python

### Data Analysis

* Pandas
* NumPy

### Visualization

* Matplotlib
* Seaborn

### Machine Learning

* Scikit-Learn
* XGBoost

### Statistical Testing

* SciPy

### Development Environment

* Jupyter Notebook

---

## Future Enhancements

* Hyperparameter tuning using GridSearchCV
* Deployment using Streamlit
* Real-time churn monitoring dashboard
* Customer Lifetime Value (CLV) prediction
* Explainable AI using SHAP values

---

## Author

**Milan Manoj**

Aspiring Data Analyst | Business Intelligence Enthusiast | FinTech Analytics

Skills:

* SQL
* Python
* Power BI
* Tableau
* Machine Learning
* Statistical Analysis
* Business Analytics

