1. **Alternative measures of risk**
Let's discuss some alternative measures of risk.

2. **Looking at downside risk**
When we use measures such as standard deviation and variance for volatility, it measures all deviations from the mean, so both upside and downside deviations. However, investors typically don't lose sleep over gains in their portfolios. They do however worry about negative returns. That suggests that a good risk measure should perhaps focus on the potential losses, rather than overall fluctuations measured by volatility.

3. **Sortino ratio**
That's where the Sortino ratio comes in. The Sortino ratio is a variation of the Sharpe ratio. It differentiates harmful volatility from overall volatility by using the asset's standard deviation of negative portfolio returns only. So instead of the normal standard deviation, in the Sortino ratio you calculate the standard deviation of the negative returns only, called downside risk.

4. **Sortino ratio in python**
If you follow the formula in the previous slide, the Sortino ratio is very easily calculated. Let's have a look at the Apple stock again. First, define the risk-free rate and the target return for the stock, let's assume both are zero. Then, let's calculate the daily returns from the prices, and save those in a DataFrame. Now you create a new DataFrame, which stores the negative return numbers only. I'm using the .loc function for this on the apple returns data, and select the negative returns below the target using the mathematical symbol for "strictly less than".

5. **Sortino ratio in python**
Now let's, for the sake of simplicity, take the mean return of the apple returns for the expected return. Be careful not to calculate the mean on the negative returns, that would be wrong. And for the standard deviation, let's calculate that using the newly created negative returns DataFrame. These are all the ingredients we need for the Sortino ratio calculation, which looks just like the Sharpe ratio. There you have it.

6. **Maximum draw-down**
Maximum draw-down refers to the largest percentage loss from a market peak to trough. A large draw-down is usually followed by investors fleeing a fund, leading to more losses. Hence, most investors will look at previous draw-downs to assess the risk. In the graph here you see historic data on the S&P500 between 1994 and 2010. The maximum draw-down is -53% during the financial crisis, which is significant. The maximum draw-down depends very much on the chosen time window: a narrow time window will likely have smaller draw-downs. Also remember that there is asymmetry in draw-downs and gains: losing 50% requires future gains of 100% or more just to break even. The time it takes to get back to break-even is called the recovery time. In the graph you see that the first draw-down has a pretty long recovery time in fact.

7. **Maximum daily draw-down in Python**
In order to calculate the maximum draw-down, you need to work with rolling windows, which you might have come across in the "Manipulating Time Series Data in Python" course. First, you need to find the maximum value in the time series, using a 250 trading day window, this equals 1 year of trading. Use min_periods=1 if you want to start calculating from day 1, and let the first 250 day window simply expand. Now calculate the daily draw-downs by comparing the prices to their rolling max. Simply pick the rolling smallest number from those daily draw-downs using the rolling.min function. Since these numbers are negative, the smallest number actually gives you the biggest draw-down. Now let's plot the results.

8. **Maximum draw-down of Apple**
And there you have it, here is the plot of the daily draw-downs in blue, and the plot that picks the biggest draw-down up until that point in green. Do you see that the lowest draw-down is around May 2016, I've added a red circle at the maximum draw-down? This is where the green line dips the lowest for the first time.

9. **Let's practice!**
Let's practice!