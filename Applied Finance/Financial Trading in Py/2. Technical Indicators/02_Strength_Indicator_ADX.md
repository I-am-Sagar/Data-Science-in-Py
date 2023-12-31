1. **Strength indicator: ADX**
In this lesson, we will learn about a popular trend strength indicator called Average Directional Movement Index or ADX.

2. **What is ADX?**
ADX stands for "Average Directional Movement Index". It was developed by J. Welles Wilder, who elaborated the concept in his famous book "New Concepts in Technical Systems". Wilder created ADX with the intention to measure the strength of a trend objectively. ADX can indicate whether an asset price is trending or merely moving sideways. However, it does not tell the direction of a trend, that is bullish (rising prices) or bearish (falling prices). ADX oscillates between 0 and 100. In general, an ADX less than 25 indicates the market is going sideways and has no clear trend. An ADX above 25 indicates the market is trending, and an ADX above 50 suggests a strong trending market.

3. **How is ADX calculated?**
ADX is obtained using lengthy and complicated calculations. Simply put, ADX is derived from two other indicators: plus DI and minus DI. The plus DI, or plus directional index, quantifies the presence of an uptrend; and the minus DI, or minus directional index, quantifies the presence of a downtrend. ADX is the smoothed averages of the difference between plus DI and minus DI. The calculation input for ADX includes the high, low and close prices of each period.

4. **Implementing ADX in Python**
ADX can be implemented in Python by calling talib dot ADX, and passing three types of price data as input, the high, low and close price. Originally Welles Wilder used a 14-period lookback window for ADX calculations, which became the industry standard. You can change the default period with the timeperiod parameter. Keep in mind, the longer the lookback window, the less sensitive the ADX is to the price fluctuations. In other words, a 14-day ADX is more sensitive to daily price changes than a 21-day ADX. Sometimes traders change the lookback period to suit their trading time horizons. For example, a position trader who holds a trading position for several months would likely use a longer lookback period. In this sample code, we calculate ADX and save it in a new DataFrame column. We can use dot tail to check the last 5 rows.

5. **Plotting ADX**
Usually, an ADX plot is placed horizontally under a price plot, so we can observe the price and indicator changes together along the same timeline. This can be accomplished by using the matplotlib subplots function. In this sample code, we create a set of subplots, ax1 and ax2, to plot the price and ADX separately. We can also use set underscore ylabel to label the y axis of each subplot for more clarity. Notice in the chart, the ADX starts to rise when the price is steadily trending up. The ADX starts to decline when the uptrend in price is stalling and price is moving sideways.

6. **Let's practice!**
Awesome! Now let's practice!