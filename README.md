# Make-Money-in-Stocks
In Wall Street, the global financial center, the proportion of investment in artificial intelligence has increased gradually since the 2008 financial crisis (Source: Bloomberg)
In addition, artificial intelligence can make reasonable decisions because it does not pay for the inefficiency of investment sentiment in determining whether to invest and scale.(E.g, The one AI system at the time of the global financial crisis in 2008 recorded a 681% )

## Dataset 
We will use each of historical stock price dataset from the Reuters. The dataset contains the raw time-series data(Open, High, Low, Close, and Volume). <br /> 

## Details of Dataset and Models 
<p align="center"> 
<img src="https://github.com/Zeng-Shuang/Make-Money-in-Stocks/blob/main/images/overview-of-strategy.png"  width="600">
</p>

+ There are 10 stocks dataset(From 2015 ~ From 2017) and KOSPI index.<br /> 
+ We use 10 stocks,KOSPI dataset not only 2015/2016(Jan-Dec) as train/Validation dateset, also 2016/2017(Jan-Dec) as test dateset.<br /> 
+ We use XGBoost model.
**Official website: https://xgboost.readthedocs.io/en/latest/index.html<br /> 

+ XGBoost and other ensemble models is one of learning methods to predict stock prices. Afterwards based on past market data, stocks (listed in KOSPI market) are subject to post-verification(back-testing) and real-time simulation investment.<br /> 

+ We calculate rates of each stock of returns every at the end of each week.<br /> 
## Results

+ This is the result of stock predictions. (For details, Please refer the code "LSTM-Predict_final.ipynb")
<p align="center"> 
<img src="https://github.com/Zeng-Shuang/Make-Money-in-Stocks/blob/main/images/lstm-predict.png"  width="600">
</p>


## Requirements 
+ XGboost (0.7)
+ numpy (1.15.1)
+ matplotlib (2.2.2)
+ scikit-learn (0.19.1)
+ Pandas (0.22.0)
+ Scipy (1.1.0)

## Contacts
If you have any question, please contact Zeng Shuang (zengsh9@connect.hku.hk).

<br /> 
<br />

## Reference
https://github.com/jbuckley213/Stock-Trader-Q-Learning
