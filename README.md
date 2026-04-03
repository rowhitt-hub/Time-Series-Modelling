**The notebook produces:**

1. CPI time series plots

2. Seasonal decomposition plots

3. Forecast vs actual comparison

4. RMSE performance metrics

5. Residual diagnostics

   




**Interesting take from the project:**


We see that ARIMA has actually outperformed SARIMAX inspite of being a supposedly inferior model. This is due to:

1. The CPI series after differencing may already remove much of the seasonal structure.

2. The SARIMA configuration used may be slightly over-parameterized for the available data.

3. The recent CPI period (post-2015) may exhibit weaker or less stable seasonal patterns due to economic disruptions and 
structural changes.



# Consumer Price Index (CPI) Time Series Analysis

## Overview
This project performs time series analysis and forecasting on the US Consumer Price Index (CPI). It programmatically fetches macroeconomic data from the Federal Reserve Economic Data (FRED) API, performs exploratory data analysis including seasonal decomposition, and is set up to build predictive models using ARIMA and SARIMAX. 

## Features
* **Data Acquisition:** Automatically fetches the `CPIAUCSL` series (Consumer Price Index for All Urban Consumers: All Items) using the FRED API, focusing on data from January 2015 onwards.
* **Seasonal Decomposition:** Breaks down the CPI time series into its underlying trend, seasonal, and residual components using a 12-month additive model.
* **Forecasting (Prepared):** Integrates Statsmodels and Scikit-Learn to train and evaluate ARIMA and SARIMAX forecasting models using Mean Squared Error (MSE).

## Prerequisites
To run this notebook, you will need Python 3 installed along with the following libraries:
* `pandas`
* `numpy`
* `matplotlib`
* `fredapi`
* `statsmodels`
* `scikit-learn`

You can install these dependencies using pip:
```bash
pip install pandas numpy matplotlib fredapi statsmodels scikit-learn
```

## Setup and Usage
1. **Get a FRED API Key:** You will need an API key from the Federal Reserve Bank of St. Louis. You can register for one for free on the FRED website.
2. **Configure the API Key:** Open the `CPI_time_series.ipynb` notebook. In the first setup cell, locate the following line:
   ```python
   fred_key="_"
   ```
   Replace `"_"` with your actual FRED API key string.
3. **Run the Notebook:** Execute the cells sequentially. The notebook will download the necessary data, clean missing values, generate the seasonal decomposition plots, and proceed to the forecasting sections.

## Project Structure
* **CPI_time_series.ipynb:** The main Jupyter Notebook containing all the code for data ingestion, visualization, and time series modeling. 


