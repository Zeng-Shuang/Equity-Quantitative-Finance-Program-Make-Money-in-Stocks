# Make Money in Stocks
## Introduction
Part 1. Collect stock data of 50 randomly selected S&P 500 companies from five years ago, including names of companies, dates, their prices (open, high, low, close) and trading volume.<br /> 
Part 2. Categorize companies according to their sectors: Industrial, Health Care, Communication Service, IT and Consumer Staples, and find the most profitable companies in each sector.<br /> 
Part 3. Plot the trend of stock prices of different companies during the last three years sector by sector.<br /> 
Part 4. If go three months back, arrange our saving and maximize&minimize the profit based on the historical prices five years ago (except the recent three months). Suppose we have a capital fund ($10000) for starting up, establish strategies (see in Details of Dataset and Models below) and give the analysis.<br /> 
Part 5. Based on the stock price turning points of different sectors obtained in Part 3, crawling the financial news of Wall Street Journal from 2020-03-17 to 2020-03-24. Extracting the news headlines, counting the most frequently occurring words and making word cloud maps.<br /> 

## Dataset 
We will use stock prices dataset of 50 randomly selected S&P 500 companies from https://finance.yahoo.com. The dataset contains the raw time-series data(Open, High, Low, Close, and Volume). <br /> 

## Details of Dataset and Models 
<p align="center"> 
<img src="https://github.com/Zeng-Shuang/Make-Money-in-Stocks/blob/main/images/strategy%20overview.jpg"  width="600">
</p>

+ There are 50 stocks dataset(From 2017-10-01 to 2022-11-27).<br /> 
+ We use dataset from 2017-10-01 to 2022-08-26 as train dateset, and dataset from 2022-08-27 to 2022-11-27 as test dateset.<br /> 
+ We use LSTM model for stock prices prediction, and stocks are then selected for trading. (For details, Please refer the code "Part4_LSTM Prediction.ipynb")<br /> 
+ Base on the stocks selected by LSTM model, We use Moving Average Convergence Divergence Strategy. (For details, Please refer the code "Part4_MACD Strategy.ipynb")<br /> 
+ We use Mean-Variance Portfolio model for stock selection. (For details, Please refer the code "Part4_stock selection.ipynb")<br /> 
+ Base on the stocks selected by Mean-Variance Portfolio model, We use Q Reinforcement Learning Strategy. (For details, Please refer the code "Part4_Q learning.ipynb")<br /> 
+ With an initial fund of $10000, We calculate profit after 3 months by using these two strategies.<br /> 
## Results

+ This is the result of stock predictions. (For details, Please refer the code "Part4_LSTM Prediction.ipynb")
<p align="center"> 
<img src="https://github.com/Zeng-Shuang/Make-Money-in-Stocks/blob/main/images/lstm-predict.png"  width="600">

+ This is the result of the most frequently occurring words in stock price turning points (from 2020-03-17 to 2020-03-24) . (For details, Please refer the code "Part5.ipynb")
<p align="center"> 
<img src="https://github.com/Zeng-Shuang/Make-Money-in-Stocks/blob/main/images/cloudmap.png"  width="600">
</p>


## Requirements 
+ bs4 (0.0.1)
+ jieba (0.42.1)
+ xlrd (2.0.1)
+ xlwt (1.3.0)
+ pandas (1.4.2)
+ tensorflow (2.11.0)
+ numpy (1.21.5)
+ yfinance (0.1.87)
+ keras (2.11.0)
+ scikit-learn (1.1.1)
+ statsmodels (0.13.2)
+ scipy (1.7.3)
+ seaborn (0.11.2)

## Contacts
If you have any question, please contact Zeng Shuang (zengsh9@connect.hku.hk).

<br /> 
<br />

## Reference
https://github.com/jbuckley213/Stock-Trader-Q-Learning
