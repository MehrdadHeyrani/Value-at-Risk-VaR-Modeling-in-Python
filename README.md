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

Box-Jenkins approach applies ARIMA models to find the best fit of a univariate time series model that represent the stochastic process. This method is including a three steps modelling:

1) Identification: Based on the Autocorelation Function (ACF) and Partial Autocorrelation Function (PACF) it is possible to determine p, and q order of the ARIMA model. Also, we can use the Akaike Information Criterion (AIC) to identify the ARIMA order.
2) Estimation: Estimation of best ARMA(p,q) order.
3) Diagnostic checking: The ARMA process is valid when the residuals (ACF and PACF plots) are uncorrelated.




## GARCH Modeling and Volatility 

In order to model volatility, we use the Autoregressive Conditional Heteroscedasticity (ARCH) model. ARCH is a statistical model for time series data that describes the variance of the current error term as a function of the previous time periods’ error terms.
The next step is to define the second part of the error term decomposition which is the conditional variance. For this purpose, we can use a GARCH(1, 1) models.

## Volatility forecasting based on two diffrent approach:
### Fixed Rolling Window
In the Fixed Rolling Window approach, new data are added while old ones are dropped from the sample

### Expanding window
In the Expanding Window approach, new data are continuously added to the sample without dropped old data

<img src="https://user-images.githubusercontent.com/77374087/137956676-92b387d9-86e8-4c9c-9cef-10ddf1291f30.png" width="1000" height="300">



<img src="https://user-images.githubusercontent.com/77374087/135907498-6f83b1f4-1445-4e0c-886d-e1b933d0a2dd.PNG" width="600" height="300">

```
Example of Evaluation
------------------------------------------------
Rolling Window Forcasting ARCH
Mean Absolute Error (MAE): 0.000113
Mean Absolute Percentage Error (MAPE): inf
Root Mean Square Error (RMSE): 0.000438
------------------------------------------------
Rolling Window Forcasting GARCH
Mean Absolute Error (MAE): 0.00014
Mean Absolute Percentage Error (MAPE): inf
Root Mean Square Error (RMSE): 0.0005
------------------------------------------------
Rolling Window Forcasting EGARCH
Mean Absolute Error (MAE): 0.000147
Mean Absolute Percentage Error (MAPE): inf
Root Mean Square Error (RMSE): 0.000518
```


## Value at Risk (VaR) Forecasting and Backtesting

We can use the conditional variance given by the GARCH(1,1) model for the estimation of Value at Risk (VaR). For the underlined asset’s distribution properties we can use the specific distribution such as  "normal", "t", "skewnormal", "skewt". For this method Value at Risk is expressed as:

![equation](https://latex.codecogs.com/svg.image?VaR_%7B%5Calpha%20%7D=%5Cmu%20&plus;%5Chat%7B%5Csigma%20%7D_%7Bt%7Ct-1%7D%5Ctimes%20F_%7B%5Calpha%20%7D%5E%7B-1%7D) 



<img src="https://user-images.githubusercontent.com/77374087/135907697-f95fe867-c227-44a3-8e4a-5ef769f973f2.png" width="600" height="300">

<img src="https://user-images.githubusercontent.com/77374087/135907806-e61133dc-b400-4e62-85f8-10926f957e84.png" width="600" height="300">




