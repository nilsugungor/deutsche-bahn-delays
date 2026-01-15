# deutsche-bahn-delays
Exploratory Data Analysis & Time Series Forecasting of Deutsche Bahn Train Delays
This project analyzes over 2 million train ride records from Deutsche Bahn to understand delay patterns across stations, time, and station categories. The workflow combines Exploratory Data Analysis (EDA) with time series forecasting to extract insights and predict short-term delays.
Dataset
Source: Deutsche Bahn train delay dataset (via Kaggle)
Size: ~2.06 million rows, 20+ features
Key variables: arrival/departure delays, station category, location, timestamps
Exploratory Data Analysis (EDA)
Inspected data quality, missing values, and distributions
Analyzed delay distributions and identified that most delays are short (0–5 minutes)
Compared delay probability and severity across station categories
Performed temporal analysis showing higher delay probability during rush hours (16–19)
Identified stations with:
High delay frequency but low severity (systemic delays)
Low frequency but high severity (rare but critical delays)
Found a strong correlation (≈0.96) between departure and arrival delays, indicating delay propagation
Time Series Forecasting (Prophet)
Built an hourly time series for München Ost station
Trained a Facebook Prophet model with daily, weekly, yearly, and hourly seasonality
Forecasted next 24 hours of average arrival delays
Visualized trend and seasonal components to interpret delay dynamics
Key Insights
~31% of trains experience some delay, but only ~5% exceed Deutsche Bahn’s official delay threshold
Larger and medium-sized stations tend to have higher delay probabilities
Short-term delay trends can be effectively forecasted using Prophet and generalized to other stations
Tools & Libraries
Python, Pandas, NumPy
Matplotlib, Seaborn
Facebook Prophet
Google Colab, KaggleHub
