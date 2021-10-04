# StockPrediction
Predicting price of apple stocks using 4 different models: CNN, LSTM, CNN+LSTM and LSTM+Time2Vec. <br /> <br />

Data was scraped from Yahoo Finance website in csv format with python library pandas_datareader. For every trading day there are 6 values: open, close, high, low, adjusted close and volume. The close price of the stock was used to train models. <br /> <br />

The baseline is prediction that the price will not change in the next day. <br />
Metric is RMSE. <br />
Inputs are 10 last day's prices of stock and output is 1 next day. <br />
In file predicting_stocks models are trained on stock prices from 90 companies and tested on 7 (Google, Amazon, Apple...) which returned better results than baseline. <br />
In other files stock is trained on one company and trained on the same one which returned worse results than the baseline because of not having enough data for training. <br />
The difference is also in the normalization of data (in the fie predicting_stocks we used local normalization, that is (stockprice-last_days_stockprice)/last_days+stockprice and in other 2 it is global min max normalization which is worse for the case of stock price prediction (in general time series of stock prices has increasing trend). 
