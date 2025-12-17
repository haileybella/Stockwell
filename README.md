# StockWell: Measuring the Financial Wellness of S&P 500 Companies

**KWK Machine Learning x Goldman Sachs — Final Project**
**By: Hailey Muñiz**

## 📌 Overview

StockWell is a machine learning project designed to evaluate the **financial stability** of S&P 500 companies using publicly available financial metrics.

The goal is to create a **simple, transparent Financial Health Score (FHS)** that anyone can use — students, new investors, or anyone curious about company stability — without relying on private or proprietary scoring systems.

## 🎯 Research Question

**Can we use machine learning to predict a company’s near-future financial health using a few key indicators such as:**

* EBITDA (Earnings Before Interest, Taxes, Depreciation, and Amortization)
* Revenue Growth
* Current Price
* Market Capitalization

## 📊 Dataset

**Source:** S&P 500 Stocks (Larxel — Kaggle Dataset)
This dataset includes financial and company information for all S&P 500 companies.

## 🔧 Methods & Workflow

### **1. Data Cleaning**

* Filled missing values using the median
* Removed non-essential columns
* Converted categorical variables (sector, industry) into numeric form
* Standardized numeric features using **Z-score scaling**

### **2. Feature Engineering — Financial Health Score (FHS)**

Created a custom score inspired by the Altman Z-Score:

FHS = Z(Ebitda) + Z(RevenueGrowth) + Z(CurrentPrice) + Z(MarketCap)

Higher FHS → better financial health.

### **3. Modeling — Random Forest Regression**

Trained 3 models with different depths + tree counts to predict **next-period FHS**.

### **4. Evaluation Metrics**

* MAE: ~0.88–0.92
* RMSE: ~2.15
* R²: ~0.55

Model 1 (100 trees, depth 4) performed best.

## ⭐ Key Findings

### **1️⃣ Market Capitalization dominates**

It was the strongest predictor (90%+ feature importance).
→ Larger companies tend to be more financially stable.

### **2️⃣ Short-term indicators matter less**

Revenue growth, EBITDA, and stock price had much smaller influence.

### **3️⃣ Simple model performed best**

More complex models (deeper trees, more estimators) did not improve performance.

## Limitations

* Only uses **four** financial metrics
* Only includes large S&P 500 companies
* Small dataset → limits model complexity
* Market cap may overly dominate predictions
* No historical time series data

## 🚀 Future Improvements

* Add financial ratios (debt, liquidity, profitability)
* Use historical data instead of single snapshots
* Try advanced models: Gradient Boosting, XGBoost, Neural Networks
* Build scenario analysis tools (e.g., recession, interest rate changes)

## 📁 Files in This Repository

* `StockWell_Measuring_the_Financial_Wellness_of_S&P_500_Companies_(_KWK_Machine_Learning_x_Finance_Challenge)_Final_Project.ipynb` – **Main notebook** with code + results
* `StockWell Measuring the Financial Wellness of the S&P 500 (KWK Machine Learning x Finance Challenge).pdf` – Slide deck for the project
  
## 🎥 Video Presentation

**▶️ Watch the Presentation:**
https://www.tella.tv/video/stockwell-sandp-500-financial-health-scoring-3-bnoo

## Acknowledgements

This project was completed for the **KWK Machine Learning x Goldman Sachs**.
Special thanks to mentors, instructors, and open-source resources used throughout the process.
