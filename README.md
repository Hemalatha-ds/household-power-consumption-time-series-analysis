# Household Power Consumption Time Series Analysis

## 📌 Project Overview
This project performs end-to-end time series analysis on the **Household Electric Power Consumption** dataset from the UCI Machine Learning Repository. The objective is to analyze electricity usage patterns over time, extract meaningful datetime features, identify trend and seasonality, and forecast future consumption using ARIMA-based models.

---

## 📂 Dataset
- **Source:** UCI Machine Learning Repository  
- **Granularity:** Minute-level household electricity consumption  
- **Size:** ~2 million records  

## 📥 Dataset Access
The dataset is not included in this repository due to size limitations.
It can be downloaded directly from the UCI Machine Learning Repository:
Household Electric Power Consumption dataset.

### Key Variables:
- Global Active Power  
- Global Reactive Power  
- Voltage  
- Global Intensity  
- Sub-metering values  

---

## ⚙️ Workflow Summary

### 1️⃣ Data Loading & Cleaning
- Handled missing values  
- Converted numeric columns  
- Combined `Date` and `Time` into a single `Datetime` column  
- Set `Datetime` as index with minute-level frequency  

---

### 2️⃣ Datetime Feature Extraction
Extracted multiple temporal features to understand usage behavior:
- Year  
- Month  
- Day  
- Day of week  
- Hour  
- Week of year  
- Quarter  

---

### 3️⃣ Exploratory Data Analysis (EDA)
- Minute-level power consumption visualization  
- Daily average consumption trends  
- Rolling mean and rolling standard deviation  
- Correlation analysis among numerical features  

---

### 4️⃣ Trend & Seasonality Analysis
Used multiple approaches:
- Rolling statistics  
- Seasonal decomposition (additive model)  
- Visual inspection of trend and seasonal components  

---

### 5️⃣ Stationarity Check
- Augmented Dickey-Fuller (ADF) test  
- Differencing applied where necessary  

---

### 6️⃣ Time Series Forecasting
- Daily resampled data used for modeling  
- Auto ARIMA used to identify optimal parameters  
- Generated short-term and extended forecasts  
- Visualized forecasts with confidence intervals  

---

### 7️⃣ Model Evaluation
- Compared actual vs predicted values  
- Evaluated performance using MAE and RMSE  
- Residual analysis to assess model assumptions  

---

## 📊 Visualizations Included
- Minute-level consumption plot  
- Daily average power usage  
- Rolling statistics visualization  
- Seasonal decomposition plots  
- Forecast vs actual with confidence intervals  
- Residual diagnostics  

---

## 🛠️ Technologies Used
- Python  
- Pandas & NumPy  
- Matplotlib & Seaborn  
- Statsmodels  
- pmdarima  
- Scikit-learn  
- Jupyter Notebook  

---

## 📈 Key Learnings
- Importance of datetime feature engineering in time series analysis  
- Multiple techniques are required to understand trend and seasonality  
- ARIMA models are effective for short-term forecasting on aggregated data  
- Forecast uncertainty increases with longer prediction horizons  

---

## 🚀 Future Improvements
- Incorporate external factors such as weather data  
- Use rolling cross-validation for model robustness  
- Experiment with SARIMA and Prophet models  

---

## ✅ Conclusion
This project applies a structured time series analysis approach to household electricity consumption data. 
Datetime feature extraction and exploratory analysis enabled the identification of trend and seasonality patterns. 
A seasonal ARIMA model was used for forecasting, and its performance was evaluated using standard forecasting error metrics.

