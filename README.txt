This repository contains two forecasting models for the Toronto Island Ferry Ticket data:

1. Redemption_model_improved.ipynb
Forecasts Redemption Count (people who actually boarded the ferry)

Key Features:

Time-based features: dayofweek, month, is_weekend, is_holiday

Lag features: previous 1, 7, and 14 day redemption counts

Rolling window stats: 3- and 7-day means, 7-day std deviation

Trend-based features: daily and weekly differences

Models:

Baseline (Given)

XGBoost with log-transformed target

Evaluated with MAE and MAPE

Visual forecast plots for each cross-validation fold

2. sales_forecast_model.ipynb

Forecasts Sales Count (tickets sold)

Key Features:

Same feature set as the redemption model (lags, rolling stats, diffs, holidays)

Models:

XGBoost

Uses log-transformation for better handling of skewed sales

Visual evaluation + printed metrics for each model

3. Input data
Toronto Island Ferry Ticket Counts.csv

4. How to run
pip install pandas numpy scikit-learn xgboost holidays matplotlib

5. Output
Split-by-split error metrics

Line plots comparing predicted vs observed values

### Disclaimer ###
The forecasting models and documentations were partially developed using ChatGPT (Models GPT-4o/o3) by OpenAI for coding support and explanation. The final implementation and review have been done by the applicant. 