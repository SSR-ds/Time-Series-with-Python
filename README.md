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
