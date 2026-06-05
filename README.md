# 🚀 End-to-End Market Analytics & Prediction Pipeline

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 📌 Project Overview
This project demonstrates a complete, cloud-native data pipeline built entirely within Google Colab. It showcases the integration of Cloud API data extraction, exploratory data analysis (EDA), feature engineering, and predictive Machine Learning using Python. 

The pipeline dynamically fetches live financial data from the cloud, processes it to extract meaningful market trends, and trains a Random Forest Machine Learning model to predict future closing prices.

## 🛠️ Technologies & Skills Demonstrated
* **Cloud Computing:** Live data ingestion via Web APIs (`yfinance`), Cloud Storage integration (Google Drive).
* **Data Analytics & Engineering:** Data cleaning, rolling averages, volatility calculation, and feature engineering using `pandas` and `numpy`.
* **Data Visualization:** Creating professional, actionable financial charts using `matplotlib` and `seaborn`.
* **Machine Learning / AI:** Building, training, and evaluating a predictive regression model using `scikit-learn` (Random Forest Regressor).

## 🏗️ Pipeline Architecture

### 1. Cloud Data Extraction
Instead of relying on static local CSV files, this project uses the `yfinance` API to ping cloud servers and download the last 5 years of daily stock market data (defaulting to AAPL). This demonstrates live data ingestion capabilities.

### 2. Exploratory Data Analysis (EDA) & Feature Engineering
Raw data is transformed into actionable insights:
* **Moving Averages:** Calculated 20-day and 50-day moving averages to identify market trends.
* **Daily Returns:** Computed percentage changes to measure asset volatility.
* **Target Variable Generation:** Shifted closing prices to create the next day's target for the ML model.

### 3. Machine Learning (Predictive Modeling)
A `RandomForestRegressor` is deployed to find complex, non-linear relationships between the engineered features (Open, High, Low, Volume, Moving Averages, etc.) and the future price.
* **Training/Testing Split:** 80% chronological train, 20% test split to prevent data leakage.
* **Evaluation Metrics:** Mean Squared Error (MSE) and R-squared ($R^2$) Score.

### 4. Cloud Deployment
The final, cleaned, and engineered dataset is exported directly back to Cloud Storage (Google Drive) for downstream use in BI tools like Tableau or Looker.

## 🚀 How to Run the Project

1. Open [Google Colab](https://colab.research.google.com/).
2. Upload the `End_to_End_Market_Analytics_and_Prediction.ipynb` notebook (or copy-paste the provided code).
3. Go to **Runtime > Run all**.
4. *(Optional)* If prompted, grant permission to connect to your Google Drive to test the cloud storage export feature.

## 📊 Results & Visualization
The notebook automatically generates two key visualizations:
1. **Trend Analysis:** A time-series chart overlaying the actual closing prices with the 20-day and 50-day moving averages.
2. **AI Prediction Accuracy:** A comparative line chart plotting the Machine Learning model's predicted future prices against the actual historical test data.

## 🤝 Contact
Created to demonstrate end-to-end cloud, data, and ML proficiency. Feel free to reach out with any questions or connect with me on LinkedIn!
