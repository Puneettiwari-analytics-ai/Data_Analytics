[README.md](https://github.com/user-attachments/files/27955867/README.md)[Uploading READ# 👥 Employee Turnover Prediction & Retention Analytics

An end-to-end machine learning project built for **Portobello Tech's HR Department** to predict employee turnover and recommend data-driven retention strategies.

---

## 📌 Overview

The dataset (`HR_comma_sep.csv`) contains employee records including satisfaction levels, performance evaluations, project counts, monthly hours, tenure, salary, and whether the employee eventually left the company. The goal is to identify at-risk employees before they resign and classify them into risk zones for targeted HR intervention.

---

## 📂 Dataset Features

| Column | Description |
|--------|-------------|
| `satisfaction_level` | Employee satisfaction score (0–1) |
| `last_evaluation` | Last performance evaluation score (0–1) |
| `number_project` | Number of projects assigned |
| `average_montly_hours` | Average monthly hours worked |
| `time_spend_company` | Years spent at the company |
| `Work_accident` | Whether the employee had a workplace accident |
| `left` | Target — 1 if employee left, 0 if stayed |
| `promotion_last_5years` | Whether promoted in last 5 years |
| `Department` | Employee's department |
| `salary` | Salary level (low / medium / high) |

> Dataset adapted from [Kaggle HR Analytics](https://www.kaggle.com/liujiaqi/hr-comma-sepcsv)

---

## 🔍 Key Steps

| Step | Description |
|------|-------------|
| Data Quality & EDA | Checked missing values, explored distributions and key attrition drivers |
| Correlation Analysis | Heatmap of all numerical features |
| Employee Clustering | K-Means (k=3) on employees who left, based on satisfaction & evaluation |
| Class Imbalance | Applied **SMOTE** to balance the target class |
| Model Training | 5-fold cross-validation on 3 models |
| Model Evaluation | ROC-AUC, confusion matrix, classification report |
| Risk Zone Classification | Scored employees into 4 retention risk zones |

---

## 🤖 Models Used

- Logistic Regression
- Random Forest Classifier
- Gradient Boosting Classifier

> **Best model selected based on Recall** — minimizing false negatives is critical in turnover prediction (missing an at-risk employee is costlier than a false alarm).

---

## 🚦 Risk Zone Classification

| Zone | Score Range | Action |
|------|-------------|--------|
| 🟢 Safe Zone | < 20% | No immediate action needed |
| 🟡 Low-Risk Zone | 20% – 60% | Monitor and engage |
| 🟠 Medium-Risk Zone | 60% – 90% | Proactive retention efforts |
| 🔴 High-Risk Zone | > 90% | Immediate intervention required |

---

## 🛠️ Tech Stack

![Python](https://img.shields.io/badge/Python-3.x-blue)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-ML-orange)
![Imbalanced-learn](https://img.shields.io/badge/Imbalanced--learn-SMOTE-red)
![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-teal)

- **Python** · **Pandas** · **NumPy**
- **Matplotlib** · **Seaborn**
- **Scikit-learn** · **Imbalanced-learn (SMOTE)**

---

## 📁 Project Structure

```
├── employee_turnover.ipynb       # Main analysis notebook
├── HR_comma_sep.csv              # Dataset
└── README.md
```

---

## 🚀 How to Run

```bash
git clone <your-repo-url>
cd employee-turnover
pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn
jupyter notebook employee_turnover.ipynb
```
ME.md…]()
