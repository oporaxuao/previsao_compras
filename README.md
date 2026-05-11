# 🛒 Purchase Prediction — Marketing Campaign Optimization

Binary classification model to predict whether a customer will make a web purchase, enabling marketing teams to target only high-conversion profiles and maximize campaign ROI.

---

## 🎯 Business Objective

When promotions and communications are sent to the entire customer base indiscriminately, ROI drops and customers are frustrated by irrelevant offers. This project builds a predictive model that identifies — with high precision — which customers have a real propensity to buy online (`WebPurchases = 1`), allowing the company to focus marketing efforts where they will actually convert.

---

## 🔍 Key Insights (EDA)

Exploratory analysis revealed critical patterns about consumer behavior:

**Income & Spending:** Customers who buy online have a significantly higher median income (USD 64,006 vs USD 36,640 for non-buyers).

**The Power of Wine:** Wine spending represents approximately 55% of the average total spend in the dataset, making it the anchor product for upselling strategies.

**Family Impact:** Having children at home dramatically reduces online purchase propensity — the conversion rate drops from 68.4% for customers with no children to approximately 23.9% for those with two children.

**Recency:** Time since last purchase was not a strong discriminator between groups, indicating that spending volume and financial profile drive conversion more than timing.

---

## 🗂️ Methodology

### 1. Preprocessing & Feature Engineering
- Null value treatment and data type normalization
- Feature engineering from demographic and behavioral variables
- Encoding of categorical variables

### 2. Modeling
Two ensemble models based on decision trees were trained and compared: **Random Forest** and **XGBoost**.

XGBoost delivered the best performance, showing excellent ability to identify real buyers without generating excessive false positives for the marketing team.

### 3. Evaluation
Beyond standard classification metrics, results were translated into **business-level impact** — the measure that actually matters for a marketing team.

---

## 📊 Results

**Winning model: XGBoost (test set)**

| Metric | Value |
|---|---|
| F1-Score | 0.9322 |
| AUC-ROC | 0.9791 |
| Accuracy | 92.86% |
| Capture Rate | 96.9% of real buyers correctly identified |

---

## 💡 Business Recommendations

Based on Feature Importance analysis (Total Spend and Wine Spend were the most decisive factors):

**Premium Wine Campaign:** Target customers with a high model score and no children at home — maximizing conversion rate and average ticket.

**Retention with Discounts:** Direct specific offers to customers with medium score and children, aiming to prevent churn driven by changing family spending priorities.

**Digital Migration:** Run A/B tests with customers who have high in-store purchase volume, offering exclusive incentives for their first web purchase.

---

## 🚀 Next Steps

- Advanced hyperparameter optimization with `GridSearchCV` or `Optuna`
- Evaluation of synthetic data generation (SMOTE) if class distribution shifts over time
- Model deployment via REST API (FastAPI) for real-time customer scoring

---

## 🛠️ Tech Stack

| Category | Tools |
|---|---|
| Language | Python |
| Data Manipulation | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Machine Learning | Scikit-learn, XGBoost, Random Forest |
| Evaluation Metrics | F1-Score, AUC-ROC, Confusion Matrix, Feature Importance |
| Environment | Jupyter Notebook |

---

## ▶️ How to Run

```bash
# Clone the repository
git clone https://github.com/oporaxuao/purchase-prediction-ml.git
cd purchase-prediction-ml

# Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn xgboost jupyter

# Launch the notebook
jupyter notebook
```

---

## 👤 Author

**João Alfredo de Sousa Siqueira**
[![LinkedIn](https://img.shields.io/badge/LinkedIn-oporaxuao-blue)](https://linkedin.com/in/oporaxuao)
[![GitHub](https://img.shields.io/badge/GitHub-oporaxuao-black)](https://github.com/oporaxuao)
