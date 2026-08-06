
## Introduction to the notebook
This Jupyter Notebook walks through a complete customer churn prediction workflow using real-world telecom billing data. We analyze whether customers are likely to leave their service provider based on their subscription characteristics, usage history, and tenure with the company.

## Purpose of this notebook
The goal is twofold: understand what drives customer churn through exploratory analysis AND build accurate predictive models that can flag at-risk customers for retention efforts. Businesses use such insights to reduce attrition, maintain revenue stability, and improve overall customer satisfaction.

---
### Notebook Structure Overview

1️⃣ **Exploratory Data Analysis & Feature Investigation** - We use box plots for continuous numerical variables and binary column comparisons to understand patterns in the data. This helps us identify which factors most strongly correlate with churn status.

2️⃣ **Quantitative Modeling (Univariate Approach)** - Each feature is evaluated individually using Logistic Regression coefficients, helping isolate independent effects of MonthlyCharges, TotalCharges, tenure and other variables on customer retention probability.

3️⃣ **Multivariate Modeling** - Multiple regression combines all features simultaneously to capture their joint influence on churn while accounting for feature interactions and correlations among predictors (e.g., MonthlyCharges vs TotalCharges correlation test).

4️⃣ **Binary Feature Analysis** - We examine 1+ subscription service categories alongside churn status. The analysis reveals that customers subscribing to multiple services show significantly lower churn rates, supporting the brand loyalty hypothesis: more interconnected value propositions create higher switching costs and reduce willingness to leave.

5️⃣ **Model Preprocessing** - Categorical variables are one-hot encoded using ColumnTransformer with `handle_unknown='ignore'` for robustness to unseen categories. A Random Forest Classifier Pipeline is built alongside a Logistic Regression pipeline featuring StandardScaler preprocessing.

6️⃣ **Model Training & Evaluation (RandomForestClassifier vs LogisticRegression)** - Both models fit on 80% training data and validate performance via standard metrics: accuracy, precision, recall, F1 score, plus confusion matrices for interpretability of false positives/negatives in churn prediction context. RandomForestClassifier gave rise to best score out of the two models.

---
### Key Insights from the Analysis

**Customer Segments Most Likely to Churn:**  Customers with high monthly charges, low service breadth (fewer subscriptions), and short tenure are at highest churn risk. TotalCharges correlates strongly with MonthlyCharges over time—long-term customers naturally have higher total spend but also lower churn probability due to accumulated value relationship with provider.

**Business Implications for Retention Strategy:**  - **Focus on early-tenure high-value customers**: Monitor those in first year of subscription, especially if they've only taken one service plan (e.g., basic line or standalone internet). These represent prime retention investment targets where customer experience intervention could prevent costly churn events.  
- **Bundle services strategically** across segments: Customers who subscribe to multiple services exhibit significantly lower churn—cross-selling opportunities and bundled offers can increase switching barriers. 

- **Prioritize service retention**: When a customer cancels one subscription line or plan feature, the likelihood of additional cancellations increases rapidly—retain at least one anchor offering even if other services become less valuable. 
