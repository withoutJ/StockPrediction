# StockPrediction
Predicting price of apple stocks using 4 different models: CNN, LSTM, CNN+LSTM and LSTM+Time2Vec.

The baseline is prediction that the price will not change in the next day. \n
Metric is RMSE. \n
Inputs are 10 last day's prices of stock and output is 1 next day. \n
In file predicting_stocks models are trained on stock prices from 90 companies and tested on 7 (Google, Amazon, Apple...) whihc returned better results than baseline. \n
In other files stock is trained on one company and trained on the same one which returned worse results than the baseline because of not having enough data for training. \n
The difference is also in the normalization of data (in the fie predicting_stocks we used local normalization, that is (stockprice-last_days_stockprice)/last_days+stockprice and in other 2 it is global min max normalization which is worse for the case of stock price prediction (in general time series of stock prices has increasing trend). 
