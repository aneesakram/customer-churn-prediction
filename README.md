# Customer Churn Prediction

An end-to-end machine learning pipeline to identify customers at risk of churning. This project analyzes historical customer data, performs feature engineering, and trains predictive models to optimize customer retention strategies.

## 🚀 Project Overview
Customer churn occurs when customers stop doing business with a company. Predicting churn allows businesses to proactively engage at-risk customers with targeted retention campaigns. This repository features a comprehensive Jupyter notebook (`churnModel.ipynb`) covering the entire data science lifecycle.

## 📊 Workflow & Methodology

### 1. Data Exploration & Preprocessing
* **Exploratory Data Analysis (EDA):** Investigating class imbalances, feature distributions, and correlations between customer demographics, account information, and churn status.
* **Data Cleaning:** Handling missing or null values and converting data types where necessary.
* **Feature Encoding & Scaling:** Using techniques like One-Hot Encoding for categorical variables and Standard/MinMax Scaling for continuous numerical features.

### 2. Feature Engineering
* Selecting and transforming key features (e.g., tenure, monthly charges, contract types, and support tickets) to maximize model predictive power.
* Addressing class imbalance using techniques such as SMOTE (Synthetic Minority Over-sampling Technique) or adjusting class weights.

### 3. Model Training & Evaluation
Multiple machine learning algorithms are trained and compared to find the optimal solution, typically including:
* Logistic Regression (Baseline)
* Random Forest Classifier
* XGBoost / LightGBM Gradient Boosting

**Evaluation Metrics Focus:**
* **Accuracy:** Overall correctness.
* **Precision & Recall:** Minimizing false positives while ensuring as many actual churning customers are caught as possible (High Recall is crucial for churn).
* **F1-Score & ROC-AUC:** Balancing precision/recall and evaluating overall classification performance.

## 🛠️ Tech Stack & Libraries
* **Language:** Python
* **Data Analysis:** Pandas, NumPy
* **Visualization:** Matplotlib, Seaborn
* **Machine Learning:** Scikit-Learn, XGBoost
