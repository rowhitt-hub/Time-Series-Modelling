The notebook produces:

. CPI time series plots
. Seasonal decomposition plots
. Forecast vs actual comparison
. RMSE performance metrics
. Residual diagnostics

Overview:
This project performs TSA and forecasting on the US Consumer Price Index(CPI). It fetches macro-economic data from the
Federal Reserve Economic Data (FRED) API, performs EDA oncluding seasonal decomposition, and is set up to build
predictive models using ARIMA and SARIMAX.

**Interesting take from the project:**

We see that ARIMA has actually outperformed SARIMAX inspite of being a supposedly inferior model. This is due to:
. The CPI series after differencing may already remove much of the seasonal structure.
. The SARIMA configuration used may be slightly over-parameterized for the available data.
. The recent CPI period (post-2015) may exhibit weaker or less stable seasonal patterns due to economic disruptions and 
structural changes.
