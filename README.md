<H1 align="center">Machine Learning Analysis of Banking Campaigns</H1>

<p align="center">
<a href="#"><img alt="Made with Python" src="https://img.shields.io/badge/Made%20with-Python-3776AB?style=for-the-badge"></a>
<a href="#"><img alt="Machine Learning" src="https://img.shields.io/badge/Focus-Machine%20Learning-6e3931?style=for-the-badge"></a>
<a href="#"><img alt="Status" src="https://img.shields.io/badge/Status-Completed-green?style=for-the-badge"></a>
</p>


### 📘 Project Overview

As part of a personal data analytics project, this analysis explores a real-world banking marketing dataset to understand the effectiveness of phone campaigns promoting a financial product. Each customer call includes demographic information and campaign details.

Marketing managers want to identify which factors influence customer investment behavior after a phone campaign to improve targeting and optimize resources.


### 🎯 Business Objective

#### Business Questions

> What are the main factors that influence the amount invested by customers after a phone campaign?  
> Is there a linear relationship between certain explanatory variables and the invested amount?  
> How can these insights improve future marketing campaigns?

#### Goals

- Identify the most influential variables impacting deposits  
- Build a predictive model using linear regression  
- Evaluate model performance using statistical metrics  
- Provide practical recommendations for marketing teams  

### 📑 Dataset Overview

**File:** `bank_marketing.csv`

| Column | Description | Type |
|--------|------------|------|
| age | Customer age | Numeric |
| balance | Average annual account balance | Numeric |
| duration | Phone call duration (seconds) | Numeric |
| campaign | Number of contacts made during campaign | Numeric |
| education | Education level (primary, secondary, tertiary, unknown) | Categorical |
| deposit | Amount invested after campaign (target variable) | Numeric |

### 🧪 Methodology Summary

| Step | Description |
|------|------------|
| **EDA** | Inspect data structure, distributions, and missing values |
| **Cleaning** | Handle missing values and encode categorical variables |
| **Visualization** | Analyze correlations and variable relationships |
| **Modeling** | Train a Linear Regression model |
| **Performance Analysis** | Measure RMSE, MAE, MSE, and R² |
| **Insight Recomendation** | Extract business insights and recommendations |

---

### ✅ STEP 1 — Exploratory Data Analysis (EDA)

Checked dataset structure and missing values :

- 1,000 rows and 6 columns  
- Missing values in:
  - `age` (100 missing)
  - `duration` (100 missing)
- One categorical feature (`education`) requiring encoding  


### ✅ STEP 2 — Data Cleaning

- Checked dataset structure and missing values.
- Filled missing values in `age` using the median.
- Removed rows with missing values in `duration`.
- Converted the categorical variable `education` into numerical features using one-hot encoding.

### ✅ STEP 3 - Exploratory Data Analysis
The objective of the exploratory phase was to identify relationships between variables before modeling.

- Correlation matrix to identify variables associated with the target (`deposit`)
- Scatter plot to visually inspect linearity between key features and the target

### ✅ STEP 4 - Building the Prediction Model
- Split data into training and testing sets (80% / 20%).
- Built a **Linear Regression** model to predict the deposit amount.
- Input features included age, balance, duration, campaign, and encoded education variables.


###  ✅ STEP 5 - Performance Analysis
Model performance was evaluated using standard regression metrics.

**Results obtained:**
- MAE: 82.63  
- MSE: 11195.15  
- RMSE: 105.81  
- R²: 0.75

---
### 📈 Insight Recomendation

The main factor influencing the amount invested by customers after a phone campaign is the **duration of the phone call**, followed by **age**, which has a lower influence.

There is a **linear relationship** between duration and the amount invested.

Based on the analysis and predictions, the longer the phone call, the higher the deposit amount tends to be. Future phone campaigns should therefore focus on discussion topics that encourage clients to express themselves, such as a review of their banking situation, feedback on services, and their financial needs or future projects. While allowing clients to speak freely, the conversation should remain structured and guided by the caller to ensure reassurance and clarity.

Additionally, age shows a smaller influence on deposit behavior, suggesting that targeting an older age group could be an interesting strategy to test in future campaigns.


