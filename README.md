# Time-Series-with-Python

Learning Time Series from AI Engineering YouTube Videos 

1) Exploratory Data Analysis of a Time Series Dataset
    --> the main plots that give us idea of the data and dataset are 
                --> Lag Plot
                --> auto correlation plot
                --> heatmap
                --> pairplot and sometimes grouping data together will help us to have a better idea of the dataset and gain insights from them
                --> libraries such as plotly express helps us to have slider over the range of time and play with the data


2) Methods to handle missing data in time series - While there are many methods to impute missing data such as global mean and median we have to adopt a different approach for time series data
        They are bfill, ffill, Offset Method(Takes from last year and imputes it), rolling window method

3) Moving Averages - There are various types of moving averages in Time Series Concept. 
   They are Simple Moving Average, Weighted Moving Average (Multiply with weights), Exponential Moving Average (multiply with exponents from previous ones), Exponential              Smoothening (Alpha value). The best can be found out by calculationg RMSE value on the whole.
   
4) Time Series Decomposition methods - Trend, Seasonality, Noise
               Decomposition Models - Additive, Multiplicative
               For AR/MA data needs to be stationary
    
    kpss = determining whether the time series is stationary around mean or linear time. 
         c - data is stationary around a constant, ct - data is stationary around a trend
         
         Additive - Trend + Seasonality + Residual
         Multiplicative - Trend * Seasonality * Residual
         
 5) Time series function in Python: resample, diff, shift, tshift, rolling window. cumsum(expanding.sum()),expanding.mean() index.month, index.year, index.week, pct_change
 
 6) KPSS and ADF Test helps us to find whether a time series is stationary or not around a particular time period. Stationary - mean variance and auto corelation does not change     over a period of time (no seasonality found). Understanding the time series will help us to find the right model for analysis.
 
 If you leave it without any modifications the confidence interval is going to be taken as 80%, so we have to give interval width and modify it as 0.95 which sets the confidence interval to 95% or modify it as per our wish
 
    ARMA model - Auto regressive and moving average model expects time series to be stationary.
    
   if its not stationary add some trend component to it that is the 'I'. Makes the time series stationary through the process of differentiation. This is basically differentiating from the previous time series lag. Now it becomes an ARIMA model.           
    
 Hence when it is a stationary use ARMA or else use ARIMA to make it stationary (which can be over one or many time period) i.e the parameter called D.
    
    KPSS Test -->  Series is Stationary --> Null Hypothesis - p>0.05 -> Stationary
                   Series is not Stationary --> Alternate Hypothesis-- p<0.05 -> Non Stationary
                   
                   
    Adfuller -->  Series is not Stationary --> Null Hypothesis - p<0.05 -> Stationary
                  Series is Stationary --> Alternate Hypothesis-- p>0.05 -> Non Stationary
                   
                   
7) Auto ARIMA Package- 'pmdarima' package to predict values of future time series

8) Using FB Prophet - It is package that is open sourced by Facebook DS Team. Prophet is a procedure for forecasting time series data based on an additive model where non-linear trends are fit with yearly, weekly, and daily seasonality, plus holiday effects. The input is required in the form of ds: that is the input column and y: output column. In someo cases we take care of null values by using ffill or bfill like we did for the normal time series data analysis, but fb prophet takes care of the null value by its own algorithm.

9) FB Prophet also supports multivariate analysis. While the prophet takes care of the null values or missing values in the first dependent column 'y', the other dependent columns have to be imputed by us before we further go into analysis

10) Holiday modeling - 
                   
