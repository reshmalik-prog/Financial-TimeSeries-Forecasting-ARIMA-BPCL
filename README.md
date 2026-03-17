# Financial Time Series Forecasting using ARIMA (BPCL)
## Project Overview
This project performs Time series analysis and Forecasting of stock prices for Bharat Petroleum Corporation Limited using the ARIMA model, including data preprocessing, stationarity testing, and 30-day price prediction.


---

## Dataset Details

* **Stock Name:** BPCL (Bharat Petroleum Corporation Limited)
* **Source:** NSE Historical Data
* **Type:** Time Series (Daily Closing Prices)
* **Duration:** Last 1 Year
* **File:** `Dataset/BPCL_historical.csv`

---

## Data Preprocessing

The dataset was cleaned and prepared using the following steps:

* Converted date values into proper datetime format
* Set Date as index for time series analysis
* Checked and handled missing values
* Sorted data chronologically
* Extracted closing price for modeling

**Visualization:**
The closing price trend was plotted to understand patterns and fluctuations.

* Output: `Results/BPCL_Closing_Price_Trend.png`

---

## Stationarity Testing (ADF Test)

To validate whether the time series is stationary:

* Applied **Augmented Dickey-Fuller (ADF) Test**
* Result: **Non-stationary data (p-value > 0.05)**
* Action: Applied **first-order differencing (d = 1)**

---

## ACF & PACF Analysis

* ACF and PACF plots were used to determine ARIMA parameters

* Selected model: **ARIMA(1,1,1)**

* Outputs:

  * `Results/acf_plot.png`
  * `Results/pacf_plot.png`

---

## ARIMA Model Implementation

* Model built using `statsmodels` library
* Trained on historical closing prices
* Model summary generated for evaluation

**Result:**
The ARIMA model captures short-term dependencies effectively and provides reasonable predictions.

---

## Future Price Forecasting

* Forecasted next **30 days of stock prices**
* Compared predicted values with historical data

Output:

* `Results/forecast.png`

**Observation:**
The forecast shows moderate fluctuations with a relatively stable trend, indicating short-term predictability.

---

## Key Insights & Findings

* Stock price data is **non-stationary**
* Differencing is required before modeling
* ARIMA performs well for **short-term forecasting**
* Predictions are based only on historical patterns
* External factors (market news, economy) are not considered

---

## AI Ethics & Responsible Usage

* Dataset used is **publicly available stock market data**
* No personal or sensitive information involved
* This project is developed **strictly for academic purposes**
* Forecast results **must not be used for real financial decisions**

---

## Repository Structure

```
Financial-TimeSeries-Forecasting-ARIMA-BPCL
│
├── Dataset/
│   └── BPCL_historical.csv
│
├── Results/
│   ├── BPCL_Closing_Price_Trend.png
│   ├── acf_plot.png
│   ├── forecast.png
│   └── pacf_plot.png
│
├──Source Code/
│   └── TimeSeries_ARIMA_BPCL.ipynb
│
├── AI_Ethics_Declaration_Page.pdf
└── README.md
```

---

## Tools & Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Statsmodels
* GitHub

---

## Conclusion

This project demonstrates how **time series models like ARIMA** can be applied to financial data for forecasting. While effective for identifying short-term trends, the model should be used cautiously due to market uncertainties.

---

## Contact

For collaboration or queries, feel free to connect.
