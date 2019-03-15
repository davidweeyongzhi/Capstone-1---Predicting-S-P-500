Applying Deep Learning on Price Prediction

This project aims to apply Deep Learning algorithms on prediction of price level of S&P 500 index and 
compare the results with traditional modelling methods like linear regression.

For traditional modelling methods, linear regression is used. For Deep Learning algorithms,
Long Short Term Memory aka LSTM (a form of Recurrent Neural Network) is used.

The dataset consists of S&P 500 daily index levels from Mar 1957 to Mar 2017 (15120 rows, 7 columns).
The dataset was obtained from Kaggle.

The approach was to first split dataset into trainset of 70% and testset of 30%, then run linear regression against 
respective lags of 1 day, 1 week, 1 month and 1 year, and evaluate the respective Root Mean Square Error (RMSE).
A percentage of error of model is calculated by dividing RMSE with the mean of dataset values.

Seasonal decomposition and Stationary tests are conducted on dataset to find out if there are trends or seasonal
effects on dataset and if the dataset is Stationary. The results: there are trends and seasonal effects, dataset is 
non-stationary and has high auto-correlations with its lag values.

Dataset is converted to stationary by differencing the daily levels and scaled to range of -1 to 1.

LSTM is applied to stationary and scaled dataset. RMSE is measured, percentage error calculated.

Finally, LSTM is applied to non-stationary dataset. RMSE is measured, percentage error calculated.

In conclusion, Linear Regression has goods results for shorter term predictions. 
LSTM using non-stationary data yields better results than stationary data.
LSTM model is more accurate than Linear Regression (lower percentage error).





