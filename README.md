# Value-at-Risk-VaR-Modeling-in-Python
ARMA-GARCH Modeling, Volatility and Value at Risk (VaR) Forecasting in Python
## Download Data from Yahoo Finance
```
import yfinance as yf
from yahoofinancials import YahooFinancials
start_date='2010-01-01'
end_date=end='2021-09-01'

sp_data= yf.download('SPY',  # List of tickers
                      start='2010-01-01', 
                      end='2021-09-01', 
                      progress=False)
```
## ARIMA modeling

### Box-Jenkins Methodology

## GARCH Modeling and Volatility 

<img src="" width="600" height="250">


## Volatility forecasting based on two diffrent approach:

### Fixed Rolling Window
### Expanding window


## Value at Risk (VaR) Forecasting and Backtesting



