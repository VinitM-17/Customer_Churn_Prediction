# Customer_Churn_Prediction
 Predicts whether a telecom customer will churn using classification models (Logistic Regression, Decision Tree, Random Forest). Includes EDA, label encoding, confusion matrix &amp; F1-score evaluation. Built with Python, pandas, scikit-learn, matplotlib &amp; seaborn. | Beginner-friendly ML project.


# 📉 Customer Churn Prediction — Machine Learning Project

A beginner-friendly machine learning project that predicts whether a telecom customer will churn using classification models. Built as part of an Internshala ML Internship Training project.

---

## 📌 Problem Statement

Customer churn means a customer **stops using a company's service**. Losing customers is costly — acquiring new ones is far more expensive than retaining existing ones.

This project builds a **classification model** that predicts whether a customer will churn (`Yes` / `No`) based on their demographics, account details, and the services they use — helping the company take proactive steps to retain at-risk customers.

---

## 📂 Project Structure

```
PartB_Customer_Churn_Prediction/
│
├── PartB_Customer_Churn_Prediction.ipynb  # Main Jupyter Notebook
├── Customer_data.xlsx                      # Dataset
└── README_PartB_Churn.md                   # This file
```

---

## 📊 Dataset Overview

| Detail | Info |
|---|---|
| File | `Customer_data.xlsx` |
| Rows | 7,043 |
| Columns | 21 |
| Target Variable | `Churn` → Yes (will leave) / No (will stay) |
| Churn Rate | ~26.5% |

### Key Features Used

| Feature | Description |
|---|---|
| `tenure` | Number of months the customer has been with the company |
| `Contract` | Month-to-month, One year, Two year |
| `MonthlyCharges` | Monthly billing amount |
| `TotalCharges` | Total amount charged to the customer |
| `InternetService` | DSL, Fiber optic, or None |
| `OnlineSecurity` | Whether the customer has online security |
| `TechSupport` | Whether the customer uses tech support |
| `PaymentMethod` | How the customer pays (e-check, bank transfer, etc.) |
| `gender` | Male / Female |
| `SeniorCitizen` | Whether the customer is a senior citizen |
| `Partner` / `Dependents` | Family situation |

---

## 🔧 Tech Stack

- **Language:** Python 3
- **Environment:** Jupyter Notebook
- **Libraries:**

```python
pandas, numpy, matplotlib, seaborn, scikit-learn
```

---

## 🚀 How to Run

1. Clone the repository or download the files
2. Make sure `Customer_data.xlsx` is in the same folder as the notebook
3. Install required libraries:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn openpyxl
   ```
4. Open the notebook:
   ```bash
   jupyter notebook PartB_Customer_Churn_Prediction.ipynb
   ```
5. Run all cells from top to bottom (`Kernel → Restart & Run All`)

---

## 📈 Project Workflow

```
1. Understand the Problem
        ↓
2. Import Libraries
        ↓
3. Load & Explore Dataset (EDA)
        ↓
4. Data Preprocessing
   - Handle missing values (TotalCharges)
   - Label encode all categorical columns
   - Train-test split (80/20, stratified)
        ↓
5. Model Building
   - Logistic Regression
   - Decision Tree Classifier
   - Random Forest Classifier ✅ (Best)
        ↓
6. Model Evaluation
   - Accuracy, Precision, Recall, F1 Score
   - Confusion Matrix
   - Feature Importance
        ↓
7. Conclusion & Insights
```

---

## 📉 EDA Highlights

- **~26.5% of customers churned** — the dataset is moderately imbalanced
- **Month-to-month contracts** have the highest churn rate (~43%), compared to ~11% for two-year contracts
- **New customers churn more** — average tenure for churners is ~18 months vs ~38 months for retained customers
- **Higher monthly charges** are linked to higher churn — churners pay ~$74/month vs ~$61 for those who stay
- **Fiber optic internet users** churn at a higher rate than DSL or no internet users

---

## 🤖 Models & Results

| Model | Accuracy | Precision | Recall | F1 Score |
|---|---|---|---|---|
| Logistic Regression | ~80% | ~65% | ~54% | ~59% |
| Decision Tree | ~78% | ~59% | ~50% | ~54% |
| **Random Forest** ✅ | **~80%** | **~65%** | **~52%** | **~57%** |

> ✅ **Random Forest** achieved the best overall balance of accuracy and F1 score. Recall is especially important here — we want to catch as many churners as possible before they leave.

---

## 📊 Confusion Matrix (Random Forest)

```
                  Predicted: Stayed   Predicted: Churned
Actual: Stayed         ✅ TN               ❌ FP
Actual: Churned        ❌ FN               ✅ TP
```

- **True Positives** — Churners correctly identified (most valuable)
- **False Negatives** — Churners we missed (most costly for business)

---

## 🔍 Key Feature Importances (Random Forest)

1. `tenure` — How long a customer stays is the strongest churn signal
2. `MonthlyCharges` — Higher bills increase churn risk
3. `TotalCharges` — Reflects overall customer lifetime value
4. `Contract` — Short-term contracts are the biggest churn driver
5. `InternetService` — Fiber optic customers churn more

---

## 💡 Conclusions

1. **Month-to-month contracts are the #1 churn risk** — incentivizing annual contracts with discounts could reduce churn significantly.
2. **New customers need better onboarding** — customers in their first 12 months are most likely to leave.
3. **High monthly charges drive dissatisfaction** — targeted offers or loyalty discounts for high-paying customers could improve retention.
4. **Random Forest gave the best performance** across all metrics, especially in identifying actual churners.
5. **Business action:** Proactively contact customers who have month-to-month contracts, tenure under 12 months, and monthly charges above $65 — they are the highest-risk group.

---

## 👤 Author

**[Your Name]**
ML Internship Project — Internshala Trainings

---

## 📄 License

This project is for educational purposes only.
