# Forecasting the Monthly Sales/Time-Series-Modeling

## Introduction
This project focuses on leveraging historical sales data to predict the monthly demand of products for a business interested in optimizing the demand-supply ratio and fulfilling retailer demand. The main goal is to forecast the total amount of products (requested_qty) that retailers plan to order in June and July 2020, aiding in better inventory management and planning.

## Objective
The aim is to accurately forecast the requested_qty for June and July 2020, utilizing machine learning models to analyze and predict the monthly demand based on historical data.

## Libraries Used:
```
python 3
jupyter
pandas
numpy
matplotlib
pmdarima
statsmodels
```

## Exploratory Data Analysis (EDA)
An analysis of the training data, which consists of 6671 rows and 17 features from December 2017 to May 2020, revealed both numeric and categorical data types. Notably, the `sell_in_qty` and `requested_qty` for June and July 2020 are missing, indicating the need for forecasting. The dataset exhibits yearly seasonality and an overall increasing trend, necessitating a time series modeling approach for accurate forecasting.

### Steps in Analysis
1. **Convert Data to Time Series**: Preparing the dataset for time-series analysis.
2. **Visualize Time-Series and Check for Stationarity**: Identifying patterns and ensuring the data meets model assumptions.
3. **Stationarizing the Dataset**: Using de-trending and differencing techniques to address non-stationarity.
4. **Model Building and Selection**:
   - **Simple Exponential Smoothing (SES)**: Suitable for time series data without trend or seasonal components.
   - **Holt’s Linear Trend Method**: Addresses time series data with a trend component but without a seasonal component.
   - **Holt-Winters’ Seasonal Method**: Appropriate for time series data with both trend and seasonal components.
   - **SARIMA**: Advanced model suitable for time series data with trend and/or seasonal components, excelling in capturing both elements accurately.
   - **Auto-ARIMA**: Automatically fits the best ARIMA model, simplifying the process of model selection and parameter tuning.
   - **Seasonal Decomposition of Time Series (STL)**: Used for examining and modeling seasonality and trend components separately.
5. **Sales Forecast Visualization**: Generating and visualizing the forecast for June and July 2020.

## Conclusion
After testing various models, SARIMA was identified as the most accurate based on RMSE, effectively capturing the dataset's seasonality and trend. This project highlights the importance of choosing the right model based on the data's characteristics and the potential for improving forecasts through additional analysis. The forecasted average monthly requested_qty for June and July 2020 is 603,256 and 824,352, respectively, demonstrating the effectiveness of time-series forecasting in supply chain optimization.

## Future Work
- Further explore multivariate time-series analysis to incorporate more variables that may impact demand.
- Continue to refine feature engineering efforts to extract deeper insights from the data.
- Evaluate additional models and techniques to enhance forecasting accuracy.
