# 📊 Customer Retention & Churn Analysis

**Tech Stack / Tools Used:**  
![Python](https://img.shields.io/badge/Python-3.10%2B-blue) ![Power BI](https://img.shields.io/badge/Power%20BI-Desktop-yellow) ![Pandas](https://img.shields.io/badge/Pandas-Data%20Handling-lightblue) ![NumPy](https://img.shields.io/badge/NumPy-Data%20Handling-orange) ![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-red) ![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-green) ![Scikit-learn](https://img.shields.io/badge/Scikit--learn-ML-blueviolet) ![XGBoost](https://img.shields.io/badge/XGBoost-ML-yellowgreen) ![SMOTE](https://img.shields.io/badge/SMOTE-Balancing-lightgrey)

End-to-end **Customer Churn Analysis & Prediction** using IBM Telco dataset: **EDA, SMOTE + XGBoost modeling, and business insights** with CLV & Revenue-at-Risk analysis.

---

## 📖 Project Overview
Customer churn prediction is a critical challenge for subscription-based businesses. Retaining existing customers is often **more cost-effective than acquiring new ones**, and predictive analytics allows organizations to **proactively identify customers likely to leave**.

This project delivers a **complete churn analysis pipeline** using the **IBM Telco Customer Churn dataset**, including:

- 🔍 **Exploratory Data Analysis (EDA)**
- 📈 **Cohort & Profitability Analysis**
- 🤖 **Machine Learning with SMOTE + XGBoost**
- 💵 **Revenue at Risk & Customer Lifetime Value (CLV)**
- 📊 **Interactive Dashboard (Power BI)**

**Outcome:** actionable strategies to reduce churn and protect **$4M+ in projected revenue**.

---

## 📂 Dataset

| Feature | Details |
|---------|---------|
| **Source** | IBM Telco Customer Churn (Kaggle) |
| **Initial Shape** | 7043 × 21 |
| **After Cleaning** | 7032 × 22 |
| **Target Variable** | Churn (Yes/No) |
| **Engineered Features** | ARPU, RemainingMonths, ProjectedLoss |

---

## 📌 Key Questions Answered

| # | Business Question | Outcome |
|---|-----------------|---------|
| 1 | Overall churn rate | 26.6% customers churned |
| 2 | Riskiest tenure months | Months 1–6 → 47–62% churn |
| 3 | Contract type impact | Month-to-month = 43% vs. 8% (two-year) |
| 4 | Risky payment methods | Electronic check → 45% churn |
| 5 | Internet type effect | Fiber optic = high ARPU but high churn risk |
| 6 | Strongest churn correlations | +ve: Fiber optic, e-check, monthly charges <br> −ve: Tenure, two-year contracts |
| 7 | Most profitable segments | Fiber optic + long contracts → $100+ ARPU |
| 8 | Top at-risk customers | Example: 2012-NWRPA → 98% churn probability |
| 9 | Revenue at risk | $4.27M projected lifetime loss |
| 10 | Predicted CLV of top customers | $7,000+ for high-value retained customers |

---

## 🔎 Exploratory Insights
- **Early tenure = danger zone:** Month 1 churn = 61.9%, stabilizes <40% by month 6  
- **Contract type matters:** Two-year contracts → highest retention; Month-to-month → most vulnerable  
- **Payment method:** Electronic check customers → most likely to churn  
- **High-ARPU segments:** Fiber optic + long contracts = premium customers (but highest churn risk)

---

## 🤖 Machine Learning Pipeline
- **Train/Test Split:** 80/20  
- **Class Balancing:** SMOTE  
- **Model:** XGBoost Classifier  

**Performance:**
- Accuracy: 77%  
- ROC AUC: 0.81  
- Recall (churn class): 0.57  

**Top Features:**
- Electronic check  
- Fiber optic service  
- Contract type  
- Tenure  
- Paperless billing  

---

## 🚨 High-Value At-Risk Customers

| CustomerID | ARPU | Churn Prob. | CLV |
|------------|------|------------|-----|
| 1875-QIVME | 121.4 | 80.8% | $8,498 |
| 6023-YEBUP | 109.9 | 85.5% | $7,589 |
| 2369-UAPKZ | 108.3 | 74.9% | $7,261 |

**Total revenue at risk:** $4.27M

---

## 💵 Customer Lifetime Value (CLV)
- Top customer ARPU: $118–120  
- Predicted retention: 60 months  
- Predicted CLV: $7,000+ per customer  

---

## 🛠️ Tech Stack & Tools
- **Python 3.10+**  
- **Pandas, NumPy** for data handling  
- **Matplotlib, Seaborn** for visualization  
- **Scikit-learn, XGBoost, Imbalanced-learn (SMOTE)** for ML  
- **Power BI Desktop** for interactive dashboards  
- **Kaggle / Google Colab** as platform  

---

## 🚀 How to Use

### 1. Clone the repository
```bash
git clone https://github.com/cairn16/Customer-Retention-and-Churn-Insights.git
cd Customer-Retention-and-Churn-Insights
```
### 2. Install dependencies
```bash
pip install -r requirements.txt
```
### 3. Explore the dataset

- **Raw dataset:** `data/WA_Fn-UseC_-Telco-Customer-Churn.csv`  
- **Cleaned dataset:** `outputs/clean_churn_dataset.csv`  

### 4. Run the analysis notebook

- Open `notebooks/Customer_Retention_&_Churn_Insights.ipynb` in **Jupyter Notebook**, **Lab**, or **Google Colab**  
- Run all cells to reproduce:
  - Data cleaning & preprocessing  
  - Exploratory Data Analysis (plots & tables)  
  - Machine Learning pipeline (SMOTE + XGBoost)  
  - CLV & Revenue-at-Risk calculations  

### 5. Explore Power BI dashboard

- Dashboard report: `dashboard/Customer_Retention_and_Churn_Insights.pbix`  
- Interactive visualizations for revenue-at-risk, high-value customers, and churn segments  

## ✅ Business Recommendations

- **Early onboarding focus:** Retention campaigns in first 6 months  
- **Contract strategy:** Incentivize annual/two-year plans  
- **Payment optimization:** Convert e-check customers → auto-pay  
- **Fiber optic retention:** Loyalty rewards for premium fiber optic users  
- **ML-driven CRM integration:** Deploy churn scores for proactive outreach  

## 🏆 Project Takeaways

- **End-to-end pipeline:** EDA → ML → Business Value → Dashboard  
- **$4M+ revenue at risk identified**  
- **Predictive modeling enables proactive retention**  
- **Clear, actionable business recommendations**  


## 🔮 Future Work

- Extend predictive modeling to incorporate **real-time streaming data** for faster churn detection  
- Develop **additional machine learning models** (e.g., LightGBM, CatBoost) and compare performance  
- Enhance the **Power BI dashboard** with interactive filters and forecasting capabilities  
- Integrate the pipeline with **CRM systems** for automated retention strategies  
- Explore **customer segmentation using clustering** for more personalized retention campaigns  

## 📫 Contact
 **Cairn Correia**
- [LinkedIn](https://www.linkedin.com/in/cairn-correia)
- [Email](mailto:cairncorreia@gmail.com) 
