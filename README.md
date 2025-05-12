# Time-Series-Forecasting
# 📈 Financial Time Series Forecasting using SARIMA

This project focuses on analyzing and forecasting financial pricing data using a SARIMA model. It includes detailed exploratory data analysis (EDA), statistical preprocessing, and 30-day ahead forecasting using Python and Statsmodels.

---

## 🛠️ Technologies & Libraries

- **Language:** Python 3
- **Libraries:** 
  - Pandas, NumPy
  - Statsmodels (SARIMAX)
  - Scikit-learn
  - Matplotlib, Seaborn
  - Pickle

---

## 🔍 Exploratory Data Analysis (EDA)

- Explored dataset structure using `.info()`, `.head()`, `.describe()`.
- Visualized and handled **missing values** and **outliers** using heatmaps and boxplots.
- Separated features into **numerical**, **categorical**, and **datetime** groups.
- Aggregated pricing data using `groupby()` on date and category.
- Checked stationarity using rolling statistics and the **ADF test**.
- Plotted **ACF/PACF** to inform SARIMA model order.
- Performed **seasonal decomposition** to analyze trend, seasonality, and residuals.

---

## 🔁 Preprocessing

- Applied **log transformation** to stabilize variance.
- Detected outliers using **standard deviation thresholding**.
- Replaced anomalies with a **rolling median smoother** (window=5).
- Split data into **training (80%)** and **testing (20%)** sets.

---

## 📈 Model: SARIMA

- Configured SARIMA with parameters: **(3,1,2)x(1,1,1,30)**.
- Fitted model using `SARIMAX` from Statsmodels.
- Forecasted:
  - Test set values
  - 30-day forward future values
- Evaluated performance using:
  - **RMSE (Root Mean Squared Error)**
  - **MAPE (Mean Absolute Percentage Error)**

---

## 📊 Results & Visualization

- Plotted actual vs. predicted values on test data.
- Visualized 30-day forecasts with confidence.
- Decomposed time series into **trend, seasonal**, and **residual** components.
- Exported predictions and forecasts as `.csv`.

<p align="center">
  <img src="images/forecast_plot.png" alt="SARIMA Forecast" width="700">
</p>

---

## 💾 Model Persistence

- Trained SARIMA model was saved using Python’s `pickle` module for reuse.

---

