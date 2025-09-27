from src.forecasting import run_arima, run_sarima, run_prophet, run_lstm

import pandas as pd
df = pd.read_csv("data/processed/aqi.csv")
df["Date"] = pd.to_datetime(df["Date"])
df = df.set_index("Date")
ts = df["AQI"].asfreq("D")

# Forecast models
arima_result = run_arima(ts)
sarima_result = run_sarima(ts)
prophet_result = run_prophet(ts)
lstm_result = run_lstm(ts)
