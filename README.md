📊 ARIMA-Based Household Power Consumption Forecasting


📌 Overview
This project applies an ARIMA time series model to forecast daily household
electric power consumption. The focus is on building an interpretable and
statistically sound forecasting pipeline including preprocessing, model
selection, evaluation, diagnostics, and future prediction.


📁 Dataset
Individual Household Electric Power Consumption  
Source: UCI Machine Learning Repository  

🔗 Dataset Link  
https://archive.ics.uci.edu/ml/datasets/individual+household+electric+power+consumption  

🧾 Key Details  
• Original frequency: Minute-level  
• Processed frequency: Daily average  
• Target variable: Global_active_power  

⚠️ Note on Missing Values  
Although the dataset schema reports no missing values, missing observations
are encoded as '?' in the raw file and were explicitly converted to NaN
during preprocessing.


🛠️ Methodology
• Datetime parsing and indexing  
• Daily resampling of power consumption  
• Exploratory time series visualization  
• Stationarity testing using ADF test (d = 0)  
• ACF and PACF analysis for parameter selection  
• ARIMA(2,0,1) model training  
• Chronological train–test split  
• Model evaluation using RMSE and MAPE  
• Residual diagnostics  
• 180-day future forecasting with proper datetime indexing  


📈 Results
• RMSE ≈ 0.42  
• MAPE ≈ 55%  

The model captures the overall trend and level of power consumption while
smoothing short-term fluctuations, which is expected behavior for a
non-seasonal ARIMA model.


🧪 Residual Diagnostics
• Residuals fluctuate around zero with no visible trend  
• Autocorrelations lie mostly within confidence bounds  
• Residual distribution is approximately normal  

These diagnostics indicate that the model adequately captures the
underlying time series structure.


⚠️ Limitations
• Seasonality is not explicitly modeled  
• Sudden spikes and short-term volatility are not captured  
• Performance can be improved using SARIMA or ML-based models  


🧰 Tools Used
• Python  
• Pandas  
• NumPy  
• Matplotlib  
• Statsmodels (ARIMA modeling)  
• Scikit-learn (evaluation metrics)  


▶️ How to Run
Open the mlmodel.ipynb notebook and run the cells sequentially.


📄 License
MIT License


👤 Author
Sreekar P
