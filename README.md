# Exploratory Data Analysis & Time Series Forecasting of Deutsche Bahn Train Delays

This project analyzes over **2 million train ride records** from Deutsche Bahn to uncover delay patterns across stations, time, and station categories. It combines **Exploratory Data Analysis (EDA)** with **time series forecasting** to generate insights and short-term delay predictions.

---

## Dataset
- **Source:** Deutsche Bahn train delays dataset (Kaggle)
- **Size:** ~2.06 million rows, 20+ features
- **Key variables:** arrival_delay_m, departure_delay_m, station, category, arrival_plan, location data

---

## Exploratory Data Analysis (EDA)

- Assessed data quality, structure, and missing values
- Analyzed delay distributions and found that most delays are short (0–5 minutes)
- Identified that ~31% of trains experience some delay, while only ~5% exceed the official DB delay threshold
- Compared delay probability across station categories, showing higher delays in larger and mid-sized stations
- Performed temporal analysis revealing peak delay probabilities during rush hours (16:00–19:00)
- Identified stations with:
  - High delay frequency but low severity (systemic delays)
  - Low frequency but high severity (rare but critical delays)
- Found a **strong correlation (≈0.96)** between departure and arrival delays, indicating delay propagation

---

## Time Series Forecasting (Prophet)

- Created an hourly time series of average arrival delays for **München Ost** station
- Trained a Facebook Prophet model with daily, weekly, yearly, and hourly seasonality
- Forecasted **average arrival delays for the next 24 hours**
- Visualized trend and seasonal components to interpret delay dynamics

---

## Key Insights

- Most train delays are short but frequent, indicating systemic rather than extreme disruptions
- Delay likelihood increases during peak commuting hours
- Short-term delay trends can be effectively forecasted using Prophet
- The approach can be generalized to other stations and routes

---

## Tools & Libraries

- Python, Pandas, NumPy  
- Matplotlib, Seaborn  
- Facebook Prophet  
- Google Colab, KaggleHub  
