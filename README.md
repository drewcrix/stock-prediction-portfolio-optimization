# Stock Prediction and Portfolio Optimization

This project involved analyzing large scale textual and quantitative datasets, developing a probability weighted expected return model, calculating portfolio performance metrics like the sharpe ratio, annualized alpha, and maximum drawdown, and determining optimal portfolios using mean-variance optimization. 

### How it works

- Parallel Data Loading & Normalization: Efficiently loads and standardizes predictive factors across time periods.
- Factor Selection: Uses LightGBM regressors with a correlation threshold to identify the most predictive factors.
- Textual Signal Extraction: Integrates FinBERT to derive sentiment-based risk scores from financial text data. Captures sentiment momentum by incorperating change in risk score per month
- Return Prediction: Employs a Transformer-based classifier to estimate the probability of positive stock returns. 
- Magnitude Modeling: Trains dual LightGBM regressors to model positive and negative return magnitudes.
- Expected Return Forecast: Combines probabilities and magnitudes to compute probability-weighted expected returns.
- Expanding-Window Validation: Continuously retrains and tests the model on rolling time windows for realistic backtesting.
- Portfolio Optimization: Applies Markowitz mean-variance optimization to construct optimal portfolios.

### Prerequisites
- Data collection: Access to appropriate financial data such as financial sentiments, financial factors, and raw quantitative data (with stock identifiers)
- Lightning AI Link to platform (not required but decent option): https://www.lightning.ai/

## Author

Drew
