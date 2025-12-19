ARIMA-Based Household Power Consumption Forecasting

Overview
This project implements an ARIMA-based time series forecasting model to predict daily household electric power consumption. The focus is on building an interpretable forecasting pipeline including preprocessing, model selection, evaluation, diagnostics, and future prediction.

Dataset
Individual Household Electric Power Consumption dataset from the UCI Machine Learning Repository.

Original frequency: Minute-level
Processed frequency: Daily average
Target variable: Global_active_power

Dataset link:
https://archive.ics.uci.edu/ml/datasets/individual+household+electric+power+consumption

Minute-level data was aggregated to daily averages to reduce noise and improve ARIMA stability.

Methodology
• Datetime parsing and daily resampling
• Exploratory time series visualization
• Stationarity testing using ADF test (d = 0)
• ACF and PACF analysis for parameter selection
• ARIMA(2,0,1) model training
• Train–test split and performance evaluation
• Residual diagnostics to validate model assumptions
• 180-day future forecasting with proper datetime indexing

Results
RMSE: ~0.42
MAPE: ~55 percent

The model captures overall trend and level while smoothing short-term fluctuations, which is expected behavior for non-seasonal ARIMA models.

Limitations
• Seasonality is not modeled
• Sudden spikes and volatility are not captured
• Advanced models like SARIMA or machine learning approaches can improve performance

Tools Used
Python
Pandas
NumPy
Matplotlib
Statsmodels (ARIMA modeling)
Scikit-learn (evaluation metrics)

How to Run
Open the mlmodel.ipynb notebook and run the cells sequentially.

License
MIT License

Author
Sreekar P

