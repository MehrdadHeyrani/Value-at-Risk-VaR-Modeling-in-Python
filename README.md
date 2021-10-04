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



## Volatility forecasting based on two diffrent approach:

### Fixed Rolling Window
### Expanding window
<img src="https://user-images.githubusercontent.com/77374087/135907498-6f83b1f4-1445-4e0c-886d-e1b933d0a2dd.PNG" width="600" height="300">


## Value at Risk (VaR) Forecasting and Backtesting

<img src="https://user-images.githubusercontent.com/77374087/135907697-f95fe867-c227-44a3-8e4a-5ef769f973f2.png" width="600" height="300">

<img src="https://user-images.githubusercontent.com/77374087/135907806-e61133dc-b400-4e62-85f8-10926f957e84.png" width="600" height="300">




