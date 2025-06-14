# alpha-insurance-risk-analytics
# 🚗 Insurance Risk Analysis – Task 1: Exploratory Data Analysis (EDA)

Welcome to the repository for analyzing insurance risk data as part of the Alpha Analytics Project. This `task-1` branch contains exploratory analysis and visual insights extracted from a large dataset of insurance transactions.

---

## 🔍 Task Overview

**Objective**: Perform exploratory data analysis (EDA) to understand the structure, quality, variability, and key patterns in the insurance dataset.

**Data Size**: ~1 million rows  
**Key Columns**:
- `TotalPremium`
- `TotalClaims`
- `SumInsured`
- `CustomValueEstimate`
- `TransactionMonth`, `Province`, `CoverType`, `AutoMake`

---

## 📈 Key EDA Highlights

### 1. 📊 **Descriptive Statistics**
- Calculated summary stats using `.describe()` for all major numerical features.
- Examined variability using standard deviation.
- Verified and cleaned column data types, especially datetime parsing.

### 2. 🔍 **Data Quality Assessment**
- Checked for and reported missing values.
- Ensured clean formatting for categorical and datetime columns.

### 3. 🧮 **Univariate Analysis**
- Plotted histograms for:
  - `TotalPremium`, `TotalClaims`, `SumInsured`
- Plotted bar charts for:
  - `Province`, `CoverType`, `AutoMake`

### 4. 🔄 **Bivariate/Multivariate Trends**
- Analyzed **Monthly Total Claims vs Total Premiums**
- Explored how **claim frequency** changes over time
- Plotted multi-line charts grouped by **Province** to detect regional patterns

### 5. 🗺️ **Geographical Comparison**
- Visualized how **Cover Type, Auto Make, Premiums** differ across `Province`

### 6. ⚠️ **Outlier Detection**
- Used box plots to detect outliers in `TotalClaims`, `TotalPremium`, and `SumInsured`.

---

## 📸 Visualizations

Here are 3 key visual insights:

1. 📉 **Monthly Total Claims and Premiums**  
   _Shows how business volumes fluctuate over time._

2. 📈 **Claim Frequency Over Time**  
   _Tracks how often claims occur each month._

3. 🌍 **Monthly Claims by Province**  
   _Reveals regional differences in claim patterns._

---

## 🗂️ Repository Structure

│
├── insurance_eda.ipynb # Main notebook with all EDA steps
├── README.md # This file
├── assets/ # (Optional) Plots/images used in EDA
└── data/ # (Optional) Cleaned/processed data

## 🧑‍💻 Author

Created by Tinsae Dagne 
For Alpha Analytics Risk Project – Week 3