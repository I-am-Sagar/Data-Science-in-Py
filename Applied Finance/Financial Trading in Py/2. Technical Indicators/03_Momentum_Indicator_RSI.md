1. **Momentum indicator: RSI**
In this lesson, let's discuss a popular momentum indicator called Relative Strength Index or RSI.

2. **What is RSI?**
RSI stands for Relative Strength Index. It was also developed by Welles Wilder. RSI has been the most popular indicator used to measure momentum, which is the speed of rising or falling in prices. The RSI oscillates between 0 and 100. Traditionally an RSI over 70 indicates an overbought market condition, which means the asset is overvalued and the price may reverse. An RSI below 30 suggests an oversold market condition, which means the asset is undervalued and the price may rally.

3. **How is RSI calculated?**
The RSI calculation follows a straightforward formula. RS, or Relative Strength, is the average of the upward price changes over a chosen n periods, divided by the average of downward price changes over those n periods. The formula is constructed in such a way that an RSI is bounded between 0 and 100.

4. **Implementing RSI in Python**
RSI can be implemented in Python by calling talib dot RSI and passing the price column. Similar to the ADX, Welles Wilder used a 14-period lookback window for RSI calculations, which became the industry standard. You can change the default period with the timeperiod parameter. Note the longer the lookback window, the less sensitive the RSI is to the price fluctuations. Traders may want to change the default time period to suit their specific trading time horizons, or as a variable input for testing different trading strategies. In this sample code, we calculated the RSI and saved it in a new DataFrame column. We can use dot tail to check the last 5 rows.

5. **Plotting RSI**
Similar to the ADX, it is helpful to plot the price and the RSI one above another. In this sample code, we created two subplots, the top plot shows the price, and the bottom plot shows the RSI. Notice in the chart, when the RSI is falling near 30, the price bottoms out and gradually recovers, and when the RSI value is approaching 70, the price reaches new highs and is more likely to pull back.

6. **Let's practice!**
Great! Now let's practice!

