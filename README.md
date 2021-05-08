# Assignment2
Ref: 《华泰金工量化资产配置7月月报：北向资金走向预示市场短期或震荡》（2020.8）

## Main Idea
The China Securities Regulatory Commission approved the Shanghai-Hong Kong Stock Connect and Shenzhen-Hong Kong Stock Connect in 2014 and 2016, respectively, and established an interconnection mechanism for the mainland and Hong Kong stock markets. The market usually refers to the combined inflow of the Shanghai-Hong Kong Stock Connect and the Shenzhen-Hong Kong Stock Connect as northbound capital. In other words, the capital going north refers to the capital flowing into the mainland stock market from Hong Kong, while the capital flowing into the Hong Kong stock market from the mainland is called the capital going south. The market widely believes that northbound capital are "smart money", which will have a certain indication effect on the short-term trend of the market. Based on such idea, my assignment conducts a statistical analysis of this indicator, construct a stock market timing strategy based on northbound funds, and conduct historical backtests. The results show that northbound capital have a good predictive effect on judging the rise and fall of the Shanghai and Shenzhen 300 Index.

## Statistic Analysis
Correlation matrix(From 2016.1.1 to 2021.5.7):  
![2021-05-08_162521](https://user-images.githubusercontent.com/78809297/117532826-13a3b200-b01c-11eb-944a-c730020fd5e0.png)

Correlation matrix(120 days rolling on 2021.5.7):  
![2021-05-08_162534](https://user-images.githubusercontent.com/78809297/117532890-58c7e400-b01c-11eb-8245-b5b0dff1f5e4.png)

There is a certain positive correlation between northward funds and the return rates of major indexes，so it can be concluded that the size of the northbound capital has a certain indicating effect on the index rate of return.

Let's take the Shanghai and Shenzhen 300 Index as an example to fit the regression line of the two scatter plots. The graph once again supports the positive correlation between northbound capital and the Shanghai and Shenzhen 300 Index.

![ZKmJc0qmPG72N1ryXwF0MEI3gCgTsVabocWq8lmZoVihikAtBTBGwAAQIJwtikAAECCELwBAAAkCMEbAABAghC8AQAAJAjBGwAAQIL8P1kwctYIm3sWAAAAAElFTkSuQmCC](https://user-images.githubusercontent.com/78809297/117533020-f6bbae80-b01c-11eb-9c56-dda558ea136c.png)

Let's look at the volatility of the Shanghai and Shenzhen 300-day yield and the northbound capital. There is a certain degree of synchronization.
![rV0AAAAAElFTkSuQmCC](https://user-images.githubusercontent.com/78809297/117533051-1fdc3f00-b01d-11eb-8fab-ffa1c7da618d.png)

Finally, it examines the correlation between the CSI 300 rate of return and the northbound capital. The data shows that from 2016 to May 2021, the average value of the correlation coefficient between the two is 0.45, and the maximum value is 0.7. The graph shows that the correlation between the two has gradually increased in recent years.
![aJhcTVG3iAAAAABJRU5ErkJggg==](https://user-images.githubusercontent.com/78809297/117533125-99742d00-b01d-11eb-8752-c3d236a65c18.png)

## Strategy Backtest
From the above analysis, we can see that there is a certain positive correlation between the northbound capital and the major indexes in the short and medium term. The following refers to the idea of the reference paper, based on the northbound capital change data to construct the Bollinger Band timing strategy, and the timing model Perform back-test analysis.

The strategy is as follows:
(1) When the scale of the northbound capital inflow on that day> the average value of the northbound capital in the past 252 trading days + 1.5 times the standard deviation, then buy the CSI 300 in the whole position;
(2) When the scale of the inflow of northbound funds on that day <the average value of northbound funds in the past 252 trading days-1.5 times the standard deviation, then liquidate the CSI 300;
(3) Buy at the opening price of the next day (the paper is measured at the closing price).

![btw85t2bcPO7dl3z7svH7mMGGLnPogZ8y+7dm4Lfv2Yee27NuHnduybx92Xj+Tn7BJkiRJ0rqa6rb+kiRJkrT2nLBJkiRJ0kQ5YZMkSZKkiXLCJkmSJEkT5YRNkiRJkibqHwYGgJLk2AtvAAAAAElFTkSuQmCC](https://user-images.githubusercontent.com/78809297/117533190-143d4800-b01e-11eb-981a-38913def2004.png)

Back-testing target: CSI 300  
Backtest period: 20170125—20210508  
Strategy annual win rate: 60.0%  
Strategy monthly win rate: 63.83%  
Strategy Weekly Win Rate: 61.04%  
Total return: Strategy: 97.66%, CSI 300: 48.5%  
Annualized rate of return: Strategy: 18.41%, CSI 300: 10.3%  
Maximum drawdown: Strategy: 17.29%, CSI 300: 32.46%  
Strategy Alpha: 0.13, Beta: 0.48, Sharpe Ratio: 2.16  


