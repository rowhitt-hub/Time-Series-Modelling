The notebook produces:

1. CPI time series plots

2. Seasonal decomposition plots

3. Forecast vs actual comparison

4. RMSE performance metrics

5. Residual diagnostics

Overview:

This project performs TSA and forecasting on the US Consumer Price Index(CPI). It fetches macro-economic data from the

Federal Reserve Economic Data (FRED) API, performs EDA oncluding seasonal decomposition, and is set up to build

predictive models using ARIMA and SARIMAX.


Interesting take from the project:


We see that ARIMA has actually outperformed SARIMAX inspite of being a supposedly inferior model. This is due to:

1. The CPI series after differencing may already remove much of the seasonal structure.

2. The SARIMA configuration used may be slightly over-parameterized for the available data.

3. The recent CPI period (post-2015) may exhibit weaker or less stable seasonal patterns due to economic disruptions and 
structural changes.
