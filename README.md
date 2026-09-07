# House Price Prediction using Regression Models

##  Project Overview

This project focuses on predicting house prices using machine learning techniques on a high-dimensional real estate dataset. It demonstrates an end-to-end Data Science workflow, including data analysis, preprocessing, feature engineering, and model optimization.


## Problem Statement

The objective is to predict the **SalePrice** of houses based on various features such as area, quality, and other structural attributes.

This is a **Regression Problem**, where the target variable is continuous.


## Dataset Information

* Dataset: House Prices - Advanced Regression Techniques (Kaggle)
* Total Records: 1460
* Total Features: 80+ (before preprocessing)

## Approach & Methodology

### 1. Data Understanding

* Explored dataset using `.head()`, `.info()`, and `.describe()`
* Identified numerical and categorical features
* Observed high dimensionality and missing values

---

### 2. Exploratory Data Analysis (EDA)

* Analyzed distribution of **SalePrice** (found it positively skewed)
* Applied **log transformation** to normalize the target variable
* Used correlation analysis to identify important features
* Visualized relationships between key variables and price

---

### 3. Data Cleaning

* Handled missing values using:

  * Context-based filling (`None` for absence-based categorical features)
  * Median imputation for numerical features
* Dropped irrelevant column: `Id`

---

### 4. Feature Engineering

* Converted categorical variables using **One-Hot Encoding**
* Handled high-dimensional data after encoding
* Prepared dataset for model training

---

### 5. Model Building

Built and compared multiple regression models:

* **Linear Regression** (Baseline Model)
* **Ridge Regression** (L2 Regularization)
* **Lasso Regression** (L1 Regularization + Feature Selection)

---

### 6. Model Evaluation

Used appropriate regression metrics:

* **RMSE (Root Mean Squared Error)**
* **R² Score**

---

## Model Performance

| Model             | RMSE | R² Score |
| ----------------- | ---- | -------- |
| Linear Regression | 0.18 | 0.83     |
| Ridge Regression  | 0.17 | 0.85     |
| Lasso Regression  | 0.16 | 0.87     |

##  Key Insights

* **OverallQual** (overall quality) is the strongest predictor of house price
* **GrLivArea** (living area) shows a strong positive relationship with price
* High-dimensional datasets benefit from regularization techniques
* Feature engineering and preprocessing significantly impact model performance


##  Technologies Used

* Python
* Pandas, NumPy
* Seaborn, Matplotlib
* Scikit-learn
