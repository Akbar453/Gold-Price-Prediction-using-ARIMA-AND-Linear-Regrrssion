# 📈 Gold Price Forecasting using ARIMA and Linear Regression

This project focuses on **forecasting gold prices** using a combination of **time series modeling (ARIMA)** and **Linear Regression** techniques. The aim is to understand the relationship between gold prices and several macroeconomic indicators and use this information to make future predictions.

---

## 📦 Dataset Information

- **Source**: [Kaggle - Gold Forecasting Dataset](https://www.kaggle.com/datasets/somyaagarwal69/gold-forecasting)
- **Size**: ~6 KB
- **Columns**:
  - `Date`: Monthly timestamps from 2000 to recent years
  - `Gold_Price`: Target variable to forecast
  - `Crude_Oil`, `Interest_Rate`, `USD_INR`, `Sensex`, `CPI`, `USD_Index`: Independent macroeconomic features

---

## 🧠 Objectives

- Explore historical trends in gold prices and their dependencies.
- Apply **Linear Regression** to understand the correlation between macroeconomic factors and gold price.
- Build an **ARIMA** model for univariate time series forecasting.
- Visualize trends, seasonalities, and evaluate model performance.

---

## 🛠️ Tools & Technologies

- Python 🐍
- Libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`, `statsmodels`, `pmdarima`
- Modeling: Linear Regression, ARIMA (Auto ARIMA for order selection)
- Visualizations: Time series decomposition, ACF/PACF plots

---

## 🚀 Installation & Setup

1. Clone the repository or download the `.ipynb` notebook.
2. Place your Kaggle API key (`kaggle.json`) in the working directory.
3. Run the following code block to download the dataset:
   ```python
   import os
   os.makedirs("/root/.kaggle", exist_ok=True)
   os.rename("kaggle.json", "/root/.kaggle/kaggle.json")
   os.chmod("/root/.kaggle/kaggle.json", 600)
   !kaggle datasets download -d somyaagarwal69/gold-forecasting
Extract the dataset:

python
Copy
Edit
import zipfile
with zipfile.ZipFile("gold-forecasting.zip", 'r') as zip_ref:
    zip_ref.extractall("gold_data")
📊 Exploratory Data Analysis
Displayed summary statistics and data preview

Visualized trends and seasonality in gold price using:

Line plots

Decomposition

ACF and PACF

📈 Modeling
✅ Linear Regression
Modeled Gold_Price based on other macroeconomic indicators.

Evaluated model performance using R-squared.

✅ ARIMA (Auto ARIMA)
Auto-identified optimal (p,d,q) parameters

Modeled gold price as a time series

Forecasted future values with confidence intervals

📉 Results
Linear Regression revealed significant correlation between gold price and variables like CPI and USD_INR.

ARIMA Model captured trends and produced reliable short-term forecasts.

Visual diagnostics confirmed model validity.

📌 Project Highlights
Demonstrates real-world forecasting use case

Combines statistical learning with machine learning

Applies feature analysis, decomposition, and forecasting models

Strong fit for use cases in finance, commodities, or macro-economic modeling

📚 References
pmdarima documentation

Statsmodels

Kaggle Dataset: Gold Forecasting

