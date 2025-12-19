════════════════════════════════════════════════════════════
 ARIMA-Based Household Power Consumption Forecasting
════════════════════════════════════════════════════════════

OVERVIEW
────────────────────────────────────────────────────────────
This project implements an ARIMA-based time series forecasting
model to predict daily household electric power consumption.
The focus is on building an interpretable and statistically
sound forecasting pipeline covering preprocessing, model
selection, evaluation, diagnostics, and future forecasting.

════════════════════════════════════════════════════════════

DATASET
────────────────────────────────────────────────────────────
Dataset Name:
Individual Household Electric Power Consumption

Source:
UCI Machine Learning Repository

Dataset Link:
https://archive.ics.uci.edu/ml/datasets/individual+household+electric+power+consumption

Key Details:
• Original frequency : Minute-level  
• Processed frequency: Daily average  
• Target variable    : Global_active_power  

Note on Missing Values:
Although the dataset schema reports no missing values, missing
observations are encoded as '?' in the raw file and were
explicitly converted to NaN during preprocessing.

════════════════════════════════════════════════════════════

METHODOLOGY
────────────────────────────────────────────────────────────
The following steps were followed in this project:

• Datetime parsing and indexing  
• Daily resampling of power consumption data  
• Exploratory time series visualization  
• Stationarity testing using Augmented Dickey-Fuller (ADF) test  
• ACF and PACF analysis for parameter identification  
• ARIMA(2,0,1) model training  
• Chronological train–test split  
• Model evaluation using RMSE and MAPE  
• Residual diagnostics to validate model assumptions  
• 180-day future forecasting with proper datetime indexing  

════════════════════════════════════════════════════════════

RESULTS
────────────────────────────────────────────────────────────
• RMSE : ~0.42  
• MAPE : ~55%  

The model captures the overall level and long-term trend of
household power consumption while smoothing short-term
fluctuations, which is expected behavior for a non-seasonal
ARIMA model.

════════════════════════════════════════════════════════════

RESIDUAL DIAGNOSTICS
────────────────────────────────────────────────────────────
• Residuals fluctuate around zero with no visible trend  
• Residual autocorrelations lie mostly within confidence bounds  
• Residual distribution is approximately normal with mild
  tail deviations  

These diagnostics indicate that the ARIMA model adequately
captures the underlying time series structure.

════════════════════════════════════════════════════════════

LIMITATIONS
────────────────────────────────────────────────────────────
• Seasonality is not explicitly modeled  
• Short-term volatility and sudden spikes are not captured  
• Forecast accuracy can be improved using SARIMA or
  machine learning-based approaches  

════════════════════════════════════════════════════════════

TOOLS USED
────────────────────────────────────────────────────────────
• Python  
• Pandas  
• NumPy  
• Matplotlib  
• Statsmodels (ARIMA modeling)  
• Scikit-learn (evaluation metrics)  

════════════════════════════════════════════════════════════

HOW TO RUN
────────────────────────────────────────────────────────────
Open the mlmodel.ipynb notebook and run the cells sequentially.

════════════════════════════════════════════════════════════

LICENSE
────────────────────────────────────────────────────────────
MIT License

════════════════════════════════════════════════════════════

AUTHOR
────────────────────────────────────────────────────────────
Sreekar P

════════════════════════════════════════════════════════════
