# Customer-Retention-and-Churn-Insights
End-to-end Customer Churn Analysis &amp; Prediction using IBM Telco dataset includes EDA, SMOTE + XGBoost modeling, and business insights with CLV &amp; Revenue-at-Risk analysis.
📊 Customer Churn Analysis & Prediction

📖 Project Overview

Customer churn prediction is a critical challenge for subscription-based businesses. Retaining existing customers is often more cost-effective than acquiring new ones, and predictive analytics allows organizations to proactively identify customers likely to leave.

This project delivers an end-to-end churn analysis pipeline using the IBM Telco Customer Churn dataset, covering:

🔍 Exploratory Data Analysis (EDA)

📈 Cohort & Profitability Analysis

🤖 Machine Learning with SMOTE + XGBoost

💵 Revenue at Risk & Customer Lifetime Value (CLV)

📊 Interactive Dashboard

✅ Outcome: actionable strategies to reduce churn and protect $4M+ in projected revenue.

📂 Dataset

Source: IBM Telco Customer Churn (Kaggle)

Initial shape: 7043 × 21
After cleaning: 7032 × 22
Target variable: Churn (Yes/No)

Engineered Features:

ARPU (Average Revenue Per User)

RemainingMonths (expected retention)

ProjectedLoss (high-value at-risk customers)

📌 Key Questions Answered
#	Business Question	Outcome
1	What is the overall churn rate?	26.6% customers churned
2	Which tenure months are riskiest?	Months 1–6 → 47–62% churn
3	How does contract type affect churn?	Month-to-month = 43% vs. 8% (two-year)
4	Which payment methods are risky?	Electronic check → 45% churn
5	How does internet type affect churn?	Fiber optic = high ARPU but high churn risk
6	What are the strongest churn correlations?	+ve: Fiber optic, e-check, monthly charges
−ve: Tenure, two-year contracts
7	Which segments are most profitable?	Fiber optic + long contracts → $100+ ARPU
8	Who are the top at-risk customers?	Example: 2012-NWRPA → 98% churn probability
9	What is the revenue at risk?	$4.27M projected lifetime loss
10	What is the predicted CLV of top customers?	$7,000+ for high-value retained customers
🔎 Exploratory Insights

Early tenure = danger zone: Month 1 churn = 61.9%, stabilizes <40% by month 6

Contract type matters: Two-year contracts → highest retention; Month-to-month → most vulnerable

Payment method: Electronic check customers → most likely to churn

High-ARPU segments: Fiber optic + long contracts = premium customers 🚨 but highest churn risk

🤖 Machine Learning Pipeline

Train/Test Split: 80/20

Class Balancing: SMOTE

Model: XGBoost Classifier

Performance:

Accuracy: 77%

ROC AUC: 0.81

Recall (churn class): 0.57

Top Features (Importance):

Electronic check

Fiber optic service

Contract type

Tenure

Paperless billing

🚨 High-Value At-Risk Customers
CustomerID	ARPU	Churn Prob.	CLV
1875-QIVME	121.4	80.8%	$8498
6023-YEBUP	109.9	85.5%	$7589
2369-UAPKZ	108.3	74.9%	$7261

📉 Total revenue at risk: $4.27M

💵 Customer Lifetime Value (CLV)

Top customer ARPU: $118–120

Predicted retention: 60 months

Predicted CLV: $7,000+ per customer

🛠️ Tech Stack

Language: Python 3.10+

Data Handling: Pandas, NumPy

Visualization: Matplotlib, Seaborn

Machine Learning: Scikit-learn, XGBoost, Imbalanced-learn (SMOTE)

Platform: Kaggle / Google Colab

🚀 Getting Started

Clone the repository:

git clone https://github.com/cairn16/Customer-Retention-and-Churn-Insights.git
cd Customer-Retention-and-Churn-Insights


Install dependencies:

pip install -r requirements.txt


Run the notebook:

Open notebooks/Customer_Retention_&_Churn_Insights.ipynb in Jupyter or Colab

Run all cells to reproduce analysis, plots, and outputs

✅ Business Recommendations

Early onboarding focus: Retention campaigns in first 6 months

Contract strategy: Incentivize annual/two-year plans

Payment optimization: Convert e-check customers → auto-pay

Fiber optic retention: Loyalty rewards for premium fiber optic users

ML-driven CRM integration: Deploy churn scores for proactive outreach

🏆 Project Takeaways

End-to-end pipeline: EDA → ML → Business Value → Dashboard

$4M+ revenue at risk identified

Predictive modeling enables proactive retention

Clear, actionable business recommendations

💡 Connects data science → business impact in a practical, measurable way 
