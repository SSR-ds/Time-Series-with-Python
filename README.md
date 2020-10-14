# Time-Series-with-Python
Learning Time Series from AI Engineering YouTube Videos 

1) Exploratory Data Analysis of a Time Series Dataset
    --> the main plots that give us idea of the data and dataset are 
                --> Lag Plot
                --> auto correlation plot
                --> heatmap
                --> pairplot and sometimes grouping data together will help us to have a better idea of the dataset and gain insights from them
                --> libraries such as plotly express helps us to have slider over the range of time and play with the data


2) While there are many methods to impute missing data such as global mean and median we have to adopt a different approach for time series data
        They are bfill,ffill,Offset Method(Takes from last year and imputes it),rolling window method
