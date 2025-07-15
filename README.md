
# 📦 Inbound Supply Chain Forecasting

This project predicts daily inbound freight volume to a distribution center using historical data. It evaluates multiple forecasting models—from traditional Linear Regression to advanced time series models like Prophet and LSTM—and compares their accuracy to support operational planning, resource allocation, and disruption management.

---

## 🚀 Project Objectives

- Forecast inbound shipment volume over time (daily granularity)
- Model weekly seasonality, linear trends, and event-driven spikes
- Compare baseline and advanced ML approaches using RMSE
- Generate actionable insights for supply chain stakeholders

---

## 🛠 Tech Stack

- **Languages**: Python (Pandas, NumPy)
- **Modeling**: Scikit-learn, XGBoost, Prophet, TensorFlow/Keras (LSTM)
- **Visualization**: Matplotlib, Seaborn
- **Feature Engineering**: Lag variables, rolling averages, cyclical encodings

---

## 🔍 Data Description

A synthetic dataset is generated to mimic real-world inbound freight patterns with:

- **Seasonality**: Weekly cycles
- **Trend**: Linear growth over time
- **Event Effects**: Peak season (Nov–Dec), disruption flags (e.g., Wednesdays in March)
- **Features**:
  - `lag_1`, `lag_7`
  - `rolling_mean_7`, `rolling_std_7`
  - `day_of_week_sin/cos`, `month_sin/cos`
  - `is_peak_season`, `is_disruption`

---

## 🧠 Models Compared

| Model              | RMSE   | Notes                                     |
|--------------------|--------|-------------------------------------------|
| **Linear Regression** | ✅ 15.40 | Best performer due to strong feature engineering |
| **Prophet**            | 16.59 | Automatically models trend + seasonality |
| **LSTM (Deep Learning)** | 25.00 | Underperformed, sensitive to training & input scope |

---

## 📈 Key Insights

- Feature engineering (lags, rolling stats, event flags) significantly boosts traditional models.
- Prophet is interpretable and good at capturing seasonal patterns but lacks external context.
- LSTM needs more tuning and extended inputs to be effective on small/medium datasets.

---

## 📊 Evaluation Metric

**Root Mean Squared Error (RMSE)** is used to evaluate model accuracy
---

## ✅ Business Value

- Helps warehouse managers plan labor and dock schedules
- Reduces demurrage costs through better volume anticipation
- Supports strategic planning for peak seasons or disruptions

