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
