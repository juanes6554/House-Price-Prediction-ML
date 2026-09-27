# House Price Prediction — Machine Learning Project

**Author:** Juan Daniel Díaz Andrade  
**Context:** Final Project - Machine Learning Crash Course / SoftServe  

---

## 📌 Project Overview

This repository contains the end-to-end development of a Machine Learning model for predicting house prices (`Price`). The project covers initial data exploration, data cleaning, feature engineering, model training, evaluation, and comparative performance analysis across multiple regression algorithms.

---

## 🎯 Objectives

- **Exploratory Data Analysis (EDA):** Analyze distributions of numerical and categorical variables.
- **Handling Missing Values:** Identify and properly impute missing data.
- **Feature Engineering:** Apply numerical feature scaling and categorical encoding (One-Hot Encoding).
- **Modeling:** Train and evaluate various regression models (Linear Regression, Ridge, Lasso, Random Forest, Gradient Boosting).
- **Evaluation:** Compare key performance metrics ($R^2$, MAE, RMSE) to select the best-performing model.

---

## 📊 Dataset Overview

The dataset contains **1,124 records** and **9 columns**, including the target variable (`Price`).

### Feature Descriptions:

| Feature | Type | Description |
|---|---|---|
| `Area_SqFt` | Numerical | Total area of the house in square feet. |
| `Rooms` | Numerical | Total number of rooms. |
| `Build_Year` | Numerical | Year the property was built. |
| `Location` | Categorical | City/Location of the property (e.g., Noida, Jaipur, Lucknow). |
| `Street_Type` | Categorical | Access/Street type (e.g., Highway Facing, Corner Plot, Main Road). |
| `Furnishing` | Categorical | Furnishing status (Furnished, Semi-Furnished, Unfurnished). |
| `Property_Type` | Categorical | Type of property (Apartment, Duplex, Villa, Independent House). |
| `Has_Pool` | Categorical | Pool presence (`Yes` / `No`). |
| **`Price`** | Numerical | **Target Variable:** Price of the house. |

---

## 🛠️ Tech Stack & Libraries

- **Language:** Python 3.12+
- **Data Analysis & Manipulation:** `pandas`, `numpy`
- **Data Visualization:** `matplotlib`, `seaborn`
- **Machine Learning:** `scikit-learn`
  - *Preprocessing:* `StandardScaler`, `OneHotEncoder`, `SimpleImputer`, `ColumnTransformer`, `Pipeline`
  - *Models:* `LinearRegression`, `Ridge`, `Lasso`, `RandomForestRegressor`, `GradientBoostingRegressor`
  - *Metrics:* `r2_score`, `mean_absolute_error`, `mean_squared_error`
- **Model Persistence:** `joblib`

---

## 🚀 Workflow Summary

1. **Data Loading & Exploratory Data Analysis (EDA):**
   - General inspection (`shape`, `info`, `describe`).
   - Missing value analysis (~2.9% missing in `Area_SqFt`, `Rooms`, and `Furnishing`).
2. **Preprocessing & Pipelines:**
   - Imputation of missing values (median for numerical, mode for categorical features).
   - Standard feature scaling for numerical variables.
   - One-Hot Encoding for categorical features.
3. **Training & Cross-Validation:**
   - Dataset splitting (`train_test_split`).
   - Cross-validation performance assessment (`cross_val_score`).
4. **Model Comparison & Selection:**
   - Test set performance comparison using error metrics to select the optimal model.
