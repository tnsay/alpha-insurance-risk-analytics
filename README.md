# 🚗 Alpha Insurance Risk Analytics – EDA and Modeling

Welcome to the repository for analyzing insurance risk data as part of the **Alpha Analytics Project**.  
This `task-1` branch focuses on **Exploratory Data Analysis (EDA)** and initial insights from a large dataset of insurance transactions.

---

## 📌 Project Overview

**Objective**: Perform EDA, identify risk patterns, and prepare data for modeling claim severity.  
**Data Size**: ~1 million records  
**Core Features**:
- `TotalPremium`, `TotalClaims`, `SumInsured`, `CustomValueEstimate`
- `TransactionMonth`, `Province`, `CoverType`, `AutoMake`

---

## 🔍 Task 1 – Exploratory Data Analysis (EDA)

### ✅ Descriptive Statistics
- Used `.describe()` to summarize major numerical features.
- Checked variability via standard deviation.
- Verified and cleaned data types (e.g., datetime parsing).

### ✅ Data Quality Checks
- Reported missing values and handled them.
- Ensured clean formatting for categorical fields.

### ✅ Univariate Analysis
- Histograms for `TotalPremium`, `TotalClaims`, `SumInsured`
- Bar plots for `Province`, `CoverType`, `AutoMake`

### ✅ Bivariate / Multivariate Trends
- Monthly trends: `Total Claims` vs `Total Premiums`
- Tracked claim frequency over time
- Multi-line charts by `Province` revealed regional patterns

### ✅ Outlier Detection
- Box plots used to flag outliers in key numeric fields

### ✅ Geographical Insights
- Compared Cover Type, Auto Make, and Premiums across provinces

---

## 📸 Visualizations

1. 📉 **Monthly Premiums vs Claims**  
   _Visualizes business volume trends over time._

2. 📈 **Claim Frequency by Month**  
   _Tracks how often claims occur monthly._

3. 🌍 **Claims by Province**  
   _Exposes regional risk distribution._

---

## 📁 Repository Structure

│
├── insurance_eda.ipynb # Main notebook with all EDA steps
├── README.md # This file
├── assets/ # Plots and images from the analysis
└── data/ # Cleaned or raw input datasets


---

## 🧪 Task 2 – Data Version Control (DVC)

- Initialized DVC for reproducible data pipelines  
- Tracked `raw_data.csv`, `cleaned_data.csv`, and derived KPIs  
- Local DVC remote set at `C:/dvc_storage`  
- Integrated DVC with Git for versioned data and models

---

## 📊 Task 3 – Statistical Risk Hypotheses

- ✅ **Provinces**: _Statistically significant differences_ in claim frequency and severity (p < 0.001)  
  ➤ *E.g., Gauteng shows ~15% higher loss ratio than Western Cape*

- ❌ **Gender**: No significant difference (p > 0.8)  
  ➤ *Gender shouldn't be a pricing factor*

---

## 🤖 Task 4 – Model Interpretability

### 🔧 Model Summary
- **Trained Model**: XGBoost Regressor  
- **Target**: `ClaimSeverity` (for claims only)  
- **Features**: Cleaned + encoded policy data  

### 🧠 SHAP for Model Explainability
```python
import shap
explainer = shap.Explainer(xgb, X_test)
shap_values = explainer(X_test)
shap.summary_plot(shap_values, X_test, max_display=10)

Model saving
import joblib
joblib.dump(xgb, "xgb_claim_severity_model.pkl")
## 🧑‍💻 Author

Created by Tinsae Dagne
For Alpha Analytics Risk Project – Week 3