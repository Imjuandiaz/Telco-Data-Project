# Telco Customer Churn and Spend Prediction

## 📌 Project Overview
This project analyzes the **Telco Customer Churn dataset** from Kaggle to build predictive models for:
- **Customer Churn (Classification)**: Predict whether a customer is likely to churn.  
- **Monthly Spend (Regression)**: Predict customer monthly charges based on demographic and service attributes.  

The goal is to generate insights into customer behavior, identify key drivers of churn, and estimate potential revenue.  

---

## 📊 Dataset
- **Source**: [Kaggle - Telco Customer Churn](https://www.kaggle.com/blastchar/telco-customer-churn)  
- **Rows**: 7,043  
- **Key Variables**:
  - CustomerID  
  - Demographics: `Gender`, `SeniorCitizen`, `Partner`, `Dependents`, `Tenure`  
  - Services: `PhoneService`, `MultipleLines`, `InternetService`, `OnlineSecurity`, `OnlineBackup`, `DeviceProtection`, `TechSupport`, `StreamingTV`, `StreamingMovies`  
  - Billing: `Contract`, `PaperlessBilling`, `PaymentMethod`, `MonthlyCharges`, `TotalCharges`  
  - Target: `Churn` (Yes/No)  

---

## 🔎 Exploratory Data Analysis (EDA)
- **Missing Values**: No missing values found.  
- **Feature Associations**:
  - Strongest predictors of **Churn**: `Contract`, `Tenure`, `OnlineSecurity`.  
  - Strongest predictors of **MonthlyCharges**: `TotalCharges`, `InternetService`, `StreamingTV`.  
- **Tools Used**:
  - `ydata-profiling` → Automated profiling report.  
  - `AutoViz` → Visual exploration.  
  - `dython` → Feature associations.  

---

## 🤖 Models

### 1. Churn Prediction (Classification)
- Framework: **PyCaret (Classification)**  
- Best Model: **AdaBoost**  
- **Performance Metrics**:
  - Accuracy: ~77%  
  - AUC: ~0.80  
- **Outputs**:
  - Confusion Matrix  
  - ROC Curve  
  - Feature Importance visualization  
  - Predictions exported to CSV  

### 2. Spend Prediction (Regression)
- Framework: **PyCaret (Regression)**  
- Best Model: **Linear Regression**  
- **Performance Metrics**:
  - R²: 0.88  
  - MAE: 10.04  
- **Outputs**:
  - Residual plots  
  - Predicted vs Actuals  
  - Predictions exported to CSV  

---

## 📂 Repository Structure
├── data/ # Dataset(s)
├── notebooks/ # Jupyter notebooks for analysis & modeling
├── scripts/ # Python scripts for reproducibility
├── reports/ # EDA reports, profiling, AutoViz outputs
├── models/ # Saved models & CSVs with predictions
├── visuals/ # ROC, Confusion Matrix, Feature Importance, etc.
├── requirements.txt # Python dependencies
└── README.md # Project documentation

📈 Key Insights

Customers with monthly contracts and no additional security services are more likely to churn.

Longer tenure reduces the probability of churn significantly.

Monthly charges are highly correlated with service bundle options (Internet, Streaming, Security).

🔮 Future Work

Try ensemble models (XGBoost, LightGBM).

Hyperparameter tuning for further optimization.

Deploy best churn model using Streamlit or Flask.

Build dashboards in Tableau or Power BI for stakeholder presentation.

🛠️ Tech Stack

Python, Pandas, NumPy

PyCaret, scikit-learn

AutoViz, ydata-profiling, dython

Matplotlib, Seaborn

✨ Author: Juan Diaz

