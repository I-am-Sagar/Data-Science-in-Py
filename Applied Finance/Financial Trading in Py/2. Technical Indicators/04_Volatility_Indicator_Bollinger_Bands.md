1. **Volatility indicator: Bollinger Bands**
In this lesson, let's learn about a very popular volatility indicator: Bollinger Bands.

2. **What are Bollinger Bands?**
Bollinger Bands are developed by John Bollinger, a famous technical trader who elaborated on the concept in his book "Bollinger on Bollinger Bands". Bollinger bands are designed to gauge price volatility, that is, price deviations from the mean. Bollinger Bands are composed of three lines: a middle band which is an n-period simple moving average line, where n equals 20 by default; and an upper and lower band that are drawn k standard deviations above and below the middle band, where k equals 2 by default. The parameters n and k can be changed. Traders may choose the n and k to suit their trading time horizons and strategy needs. For example, a trader may choose 10-period moving average and 1 point 5 standard deviations for a shorter-term strategy, or a 50-period moving average and 2 point 5 standard deviations for a longer-term strategy.

3. **Bollinger Bands implications**
Since the upper and lower bands are calculated based on standard deviations from the mean price, they adjust to volatility swings in the underlying price. The wider the Bollinger Bands, the more volatile the asset prices. In addition, Bollinger Bands intend to answer the question: is the price too high or too low on a relative basis? Statistically speaking, if the upper and lower bands are based on 1 standard deviation, they contain about 68% of the recent price moves. Similarly, if the bands are based on 2 standard deviations, they contain about 95% of recent price moves. In other words, the price only moves out of the upper or lower bands in 5% of the cases. Hence, we can say the price is relatively expensive when it is close to the upper band, and relatively cheap when it is close to the lower band.

4. **Implementing Bollinger Bands in Python**
Bollinger Bands can be implemented in Python by calling talib dot BBANDS and passing the DataFrame column, in this case, the Close price. Specify the lookback period with the timeperiod parameter, which is 20 by default. Also, use nbdevup and nbdevdn to specify the number of standard deviations away from the middle band for the upper and lower band respectively, which is 2 by default. It produces three output Series, which are, respectively, the upper band, the middle moving average line, and the lower band. They can be saved in separate variables.

5. **Plotting Bollinger Bands**
Bollinger Bands are commonly plotted on top of the price as this code demonstrates. As we can see, the Bollinger Bands become wider when the price has big upward or downward swings. When the green price data gets closer to the red upper or red lower band, it tends to reverse temporarily before continuing the original upward or downward movement.

6. **Let's practice!**
Amazing progress! Now let's practice!