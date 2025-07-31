# Bike Rental Demand Forecasting

This project focuses on predicting daily bike rental counts using weather, calendar, and seasonal data. The goal is to build and compare regression models to understand which factors influence demand and which models capture it best.

---

##  Objective

- Forecast daily bike rental demand using historical data.
- Analyze how temperature, humidity, and holidays affect rental behavior.
- Compare the performance of **Linear Regression** and **Random Forest Regressor**.

---

## Dataset Used
- **File**: `day.csv`
- **Features**:
  - **Weather-related**: `temp`, `hum`, `windspeed`
  - **Calendar-based**: `season`, `holiday`, `workingday`, `weekday`
  - **Target**: `cnt` (total number of bike rentals)

---

## Tools & Libraries

- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn

---

## Workflow Summary

1. **Exploratory Data Analysis (EDA)**
   - Trends by season, holiday, and weekday
   - Correlation heatmap
   - Temperature vs. rental count analysis

2. **Preprocessing**
   - Feature encoding
   - Dropping non-useful columns
   - Train-test split

3. **Modeling**
   - Linear Regression
   - Random Forest Regressor

4. **Evaluation**
   - MAE, MSE, RMSE, R² Score
   - Actual vs Predicted plots

---

## 📊 Evaluation Metrics

| Metric     | Linear Regression | Random Forest |
|------------|-------------------|----------------|
| MAE        | 617.39            | 429.96         |
| MSE        | 691035.01         | 458446.95      |
| RMSE       | 831.29            | 677.09         |
| R² Score   | 0.8277            | 0.8857         |

> ✅ Random Forest clearly outperforms Linear Regression by better capturing demand spikes and non-linear patterns.

---

## 📉 Key Graph Insights

### 1. 📈 **Seasonal Trends vs Bike Rentals**
<img width="580" height="455" alt="image" src="https://github.com/user-attachments/assets/5cf36979-88c6-4343-91c6-cf025dbada4e" />

### 2. 🌡️ **Temperature vs Rental Count**
<img width="714" height="470" alt="image" src="https://github.com/user-attachments/assets/7fc2dc11-607f-4725-a61c-cc25e1fb7ae5" />

### 4. 🔍 **Actual vs Predicted Comparison**
- **Linear Regression**: smooth trend but misses sharp peaks/dips.
  <img width="859" height="470" alt="image" src="https://github.com/user-attachments/assets/4d47003d-6662-4225-9846-3a75819105c6" />

- **Random Forest**: closely follows actual demand with minimal deviation.
  <img width="859" height="470" alt="image" src="https://github.com/user-attachments/assets/283e03ef-6797-4e5b-8548-a5375b6bca9b" />

After comparing the graphs of both models — Linear Regression and Random Forest, it's clear that the Random Forest model performs better.

The Linear Regression model follows the general trend, but it doesn’t capture sudden increases or drops in bike rentals very well. Its predictions are more smooth and less accurate in some places.
On the other hand,Random Forest model closely matches the actual values. The predicted line almost overlaps with the actual line, showing that it understands the data patterns more accurately.
