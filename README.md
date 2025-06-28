# 🧠 Employee Churn Prediction using Machine Learning

> Predicting employee attrition to help HR teams make proactive retention decisions.

---

## 📌 Overview

Employee churn is a major concern for organizations — it increases recruitment costs, disrupts workflows, and impacts morale. This project builds and evaluates machine learning models to **predict whether an employee is likely to leave**, using structured HR data.

The goal is to assist HR departments in identifying high-risk employees early, enabling targeted interventions and policy changes.

---

## 🔍 Problem Statement

- **Objective**: Predict whether an employee will leave (`left = 1`) or stay (`left = 0`).
- **Dataset**: HR analytics dataset with features like satisfaction level, project count, hours worked, promotions, salary level, and department.
- **Approach**: End-to-end ML pipeline from EDA to deployment-ready prediction function, with added fairness and explainability.

---

## 🛠️ Project Highlights

| Category | Details |
|---------|---------|
| 💻 Models Used | Linear Regression, Logistic Regression, Random Forest, XGBoost |
| 📊 Evaluation Metrics | Accuracy, F1 Score, ROC AUC, Confusion Matrix |
| 🔁 Class Imbalance | Handled via stratify |
| 🧪 Feature Engineering | Derived features: `recent_promotion`, `avg_hours_per_project` |
| ⚖️ Fairness Analysis | Evaluated prediction bias by salary level |
| 📈 Explainability | Feature importance (Random Forest) |
| 🚀 Deployment Ready | Includes `predict_employee_status()` function |
| 🧑‍💼 Business Use Case | Helps HR reduce turnover costs and increase retention |

---

## 📁 Project Structure

```
employee-churn/
├── employee_churn.ipynb            # Original notebook
├── README.md                       # Project documentation
├── requirements.txt                # Dependencies (optional)
└── assets/                         # Visualizations and screenshots (optional)
```

---

## 📊 Sample Results

- **Best ROC AUC**: ~0.98 (XGBoost)
- **Top Features**:
  - Satisfaction level
  - Time spent at company
  - Average monthly hours
- **Fairness**: No significant accuracy gap across salary levels (`< 0.5%`)

---

## 💡 Business Impact

For a 1,000-employee company, reducing attrition by even 10% can save **₹5–10 lakhs/month** in hiring, training, and lost productivity. This model gives HR teams early warning signals, enabling targeted retention efforts.

---

## 🧪 How to Use

```python
from churn_model import predict_employee_status

employee = {
  'satisfaction_level': 0.4,
  'last_evaluation': 0.7,
  'number_project': 3,
  ...
}

predict_employee_status(model, employee)
```

---

## ⚙️ Future Improvements

- Add Streamlit dashboard for HR teams
- Track fairness across more demographic groups (if available)
- Continuous model monitoring via A/B testing

---

## 📚 Acknowledgements

- HR analytics dataset (Kaggle/UCI)
- `scikit-learn`, `xgboost`, `seaborn`

---

## 📎 Related Links

- 📓 [Enhanced Notebook](./enhanced_employee_churn.ipynb)
- 🌐 [Streamlit App (coming soon)](#)
