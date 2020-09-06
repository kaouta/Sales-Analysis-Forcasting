# Sales-Analysis-Forcasting
For companies to become competitive and skyrocket their growth, they need to to analyse their historical Sales data to discover trends and patterns and leverage AI/ML to develop predictive models to predict sales in the future based on those historical data .
# About the work:
Given the data it is required to do some analysis on it to extract some patterns and trends that will help grow the business,then we'll do some forcasting to predict future sales 
# Data
The data contains  electronics store purchases informations broken down by month, quantity, cost, purchase address and purshase ID
# Sales analysis:
Given the data it is required to do some analysis on it to extract some insights and trend
# Steps:
we started by some data cleaning:
     - gathering all 12 month sales in on csv
     - dealing with missing values
     - changing the type of columns
     
data exploration:
in this section i tried to discover some high level business questions related to data:
     * What was the best month for sales? How much was earned that month?
     * What city sold the most product?
     * the time when the customer is more likely(maximum likelihood) to buy a product?
     * What products are most often sold ?
     * which product people need the most?(buys lot of quantity) and why?
     * what product are often sold together?(maybe we can based on the answer do some upcoming promotions)
     
     
     
# Sales forcasting:
we only took the sales and data for this step,we tried different approaches for forcasting them comparing the mean squared error to select the best fit for our data

# Naive forcast:
In this forcast technique we assume that the next expected point is equal to the last observed point so we can expect a straight horizontal line as the prediction

# ARIMA:
we started by perform Adfuller(ADF) test on our data to check if its stationary status.
ARIMA, short for 'Auto Regressive Integrated Moving Average' is actually a class of models that 'explains' a given time series based on its own past values, that is,
its own lags and the lagged forecast errors, so that equation can be used to forecast future values.

    * AR: Autoregression. A model that uses the dependent relationship between an observation and some number of lagged observations.
    * I: Integrated. The use of differencing of raw observations in order to make the time series stationary.
    * MA: Moving Average. A model that uses the dependency between an observation and a residual error from a moving average model applied to lagged observations.
Now, ACF is applied to determine the values of p,d and q variables which are to be applied in ARIMA model.
Basically ARIMA model did better than the naive forcast as it rmse is less 

# Facebook prophet:
Facebook prophet is a procedure for forecasting time series data using daily, monthly, or yearly trends for a specific occurrence like for our case regular electronic sales.
Prophet requires a two-column dataframe labeled ds and y. 
The ds column represents the datetime variables, the date that correlates to the corresponding occurrence of the y value. This y value represents the value that the program 
is learning from and is ultimately predicting the value of.

     
     
     
