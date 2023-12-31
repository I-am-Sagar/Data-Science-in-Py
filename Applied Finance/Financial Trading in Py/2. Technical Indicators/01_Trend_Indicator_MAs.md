1. **Trend indicator MAs**
Now let's learn about technical indicators!

2. **What are technical indicators?**
A technical indicator is a calculation based on historical market data, such as price, volumes, etc. They are essential to technical analysis, which assumes that the market is efficient and prices have incorporated all public information such as financial news or public policies. Traders use technical indicators to gain insight into past price patterns and to anticipate possible future price movements.

3. **Types of indicators**
There are mainly three types of indicators. Trend indicators, such as Moving Average, Average Directional Movement Index, measure the direction or strength of a trend. Momentum indicators, such as Relative Strength Index, measure the velocity of price movement, that is the rate of change in an upward or downward direction. Volatility indicators, such as Bollinger Bands, measure the magnitude of price deviations.

4. **The TA-Lib package**
We will use the TA Lib package to implement technical indicators in Python. TA Lib, which stands for Technical Analysis Library, includes over 150 indicators and is very popular among technical traders. To import the package, use import talib.

5. **Moving average indicators**
Let's start with the most commonly used trend indicators: Simple Moving average (SMA) and Exponential Moving Average (EMA). They are called "moving" averages because every average value is calculated using data points of the most recent n periods, and hence moves along with the price. Calculating the averages creates a smoothing effect which helps to give a clearer indication of which direction the price is moving - upward, downward, or sideways. Moving averages calculated based on a longer lookback period have more smoothing effects than a shorter one.

6. **Simple Moving Average (SMA)**
An SMA is the arithmetic mean of the past n prices. N is a chosen number of periods for calculating the mean. Earlier, we calculated SMA with the dot rolling dot mean method of a DataFrame. With talib, we can simply call talib dot SMA and pass the DataFrame column, in this case the Close price. Use the timeperiod parameter to specify the averaging period. Note since an n-period SMA needs at least n data points to calculate the first average value, we will get NA values for the first n minus 1 rows. Instead, we can use the tail method to check the last 5 rows.

7. **Plotting the SMA**
We can plot SMAs together with the price with matplotlib. The label is added to indicate each data series. The blue line is the SMA calculated with a shorter lookback period, and it traces the price movement closely. The red line is the SMA calculated with a longer lookback period, and is smoother and less responsive to the price fluctuations.

8. **Exponential Moving Average (EMA)**
Another popular type of moving average is the exponential moving average, or EMA. An EMA is an exponentially weighted average of the last n prices, where the weight decreases exponentially with each previous price. To implement an EMA with talib, call talib dot EMA and pass the DataFrame column as input, in this case the Close price. Similarly, specify the averaging period with the timeperiod parameter.

9. **Plotting the EMA**
As with SMAs, we see when plotting EMAs and the price data, the shorter EMA in blue is more reactive to the price movement compared to the longer EMA in red.

10. **SMA vs. EMA**
The main difference between SMAs and EMAs is that EMAs give higher weight to the more recent data, while SMAs assign equal weight to all data points. As shown in the plot containing EMA and SMA (calculated with the same lookback window), whenever the price makes a big change, the EMA in the orange line is more sensitive to the price move compared to the SMA in the blue line.

11. **Let's practice!**
Your turn to practice!

