Covid AutoRegression Model

Given a dataset containing details about new COVID-19 cases recorded in India on daily
basis as a csv file (daily_covid_cases.csv). It shows the rolling 7-day average of newly
confirmed cases starting from 30th-Jan-2020 to 2-Oct-2021. Rows are indexed with dates;
the first column represents the date and the second column represents the new COVID-19 
cases recorded that day. We will use this dataset to build an autoregression (AR) model.

-------------------------------------------------------------------------------------------

AIM:
-To generate lagged sequence with p lag and check its correlation with given sequence.

-Create scatter plot between lagged sequences and given sequence and observe.

-Take training phase as the first wave and testing phase as the second wave. Using 
 AutoRegression model, fit the model and obtain coefficients of linear combination of
 previous data using 5 day lagged values. 
 x(t+1) = w0 + w1 *x(t) +w2 *x(t-1) + … + wp *x(t-p+1).
 
-Using these coefficients predict the values for test dataset(second wave) and calculate
 rmspe and mape values.
 
-Calculate optimal lags using abs(autocorrelation)>2/sqrt(training samples)
