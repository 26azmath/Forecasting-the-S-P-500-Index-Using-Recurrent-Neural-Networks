# **Forecasting the S&P 500 Index Using Recurrent Neural Networks**

## **Project Overview**
This project investigates the effectiveness of Recurrent Neural Network (RNN) architectures in forecasting the daily closing price of the S&P 500 Index. Using over four decades of historical market data from Yahoo Finance, multiple deep learning models were implemented and evaluated to understand how well different recurrent architectures capture temporal dependencies in financial time series.

---

## **Problem Statement**
Financial time series are highly non-stationary and volatile, making accurate forecasting challenging. Traditional statistical models often fail to capture long-range dependencies. This project evaluates whether RNN-based deep learning models can improve short- and medium-term forecasting accuracy for the S&P 500 index.

---

## **Data Description**
- Source: Yahoo Finance (^GSPC)
- Time Span: ~40+ years of daily data
- Features: Open, High, Low, Close, Volume
- Records: 10,765 rows
- Data Quality: No missing values

---

## **Exploratory Data Analysis**
- Distribution analysis using histograms and boxplots
- Outlier detection using Z-score method
- Correlation analysis revealing strong multicollinearity among price features
- Feature importance analysis using Random Forest regression
- Time-series trend analysis and visualization using Tableau dashboards

---

## **Methodology**
All models use a 30-day sliding window to predict the next day’s closing price. Data was normalized using MinMaxScaler.

### **Models Implemented**
- Vanilla RNN
- LSTM
- GRU
- Bidirectional GRU
- Bidirectional RNN

Frameworks: TensorFlow / Keras

---

## **Model Evaluation**
Performance was evaluated using RMSE and MAE.

| Model | RMSE | MAE |
|------|------|------|
| Vanilla RNN | 120.34 | 89.37 |
| LSTM | 88.92 | 73.01 |
| GRU | 44.96 | 31.65 |
| **Bidirectional GRU** | **43.80** | **30.79** |
| Bidirectional RNN | 445.43 | 302.78 |

---

## **Key Findings**
- GRU-based models significantly outperform SimpleRNN architectures
- Bidirectional GRU consistently achieved the lowest error across multiple look-back windows (5, 20, 60 days)
- Gating mechanisms are critical for modeling non-stationary financial time series
- Simple RNNs underperform on long-term trend extrapolation

---

## **Business Impact**
The findings demonstrate that GRU-based architectures are suitable for short- and medium-term market forecasting, with applications in quantitative analysis, risk management, and financial decision-support systems.

---

## **Future Work**
- Incorporate exogenous variables (volume, volatility indices, macroeconomic indicators)
- Explore hybrid or attention-based architectures
- Improve long-horizon forecasting stability

---

## **Author**
Azmath Noorain  
Master’s in Advanced Data Analytics (ADTA)
