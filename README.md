Evaluating the Predictive Limits of Machine Learning in Daily Stock Return Forecasting

This project investigates whether machine learning models can effectively predict daily stock returns using historical price and volume data. The study focuses on Samsung Electronics and explores the practical limits of time-series forecasting in financial markets.

The dataset consists of historical daily stock prices, including open, high, low, adjusted close, and trading volume. Since raw price series are non-stationary and trend-driven, daily log returns were computed to create a stationary target variable suitable for modeling. Log returns provide a continuous measure of daily percentage change and are widely used in financial analysis.

Extensive exploratory data analysis was conducted to understand the structure of the series, including trend visualization, volatility inspection, and autocorrelation analysis. The results confirmed that daily returns exhibit weak serial dependence, aligning with financial theory.

A comprehensive feature engineering process was implemented, including lagged returns, rolling means, rolling volatility measures, momentum indicators, moving average ratios, and volume-based features. All features were carefully shifted to prevent data leakage.

Two machine learning models were developed and tuned using time-aware validation (TimeSeriesSplit): Random Forest and XGBoost. Hyperparameter optimization was performed using randomized search. Model performance was evaluated using Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), R², and directional accuracy.

Results show that both machine learning models significantly outperform a naive persistence baseline. Random Forest achieved approximately 52% directional accuracy while substantially reducing prediction error compared to the baseline. However, R² values remained close to zero, highlighting the inherent difficulty of predicting daily stock returns.

This project demonstrates both the capabilities and limitations of machine learning in financial time-series forecasting and reinforces the importance of proper validation and realistic interpretation of results.
