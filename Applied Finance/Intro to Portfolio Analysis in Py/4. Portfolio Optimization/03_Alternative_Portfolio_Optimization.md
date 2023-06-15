1. **Alternative portfolio optimization**
In this video we'll discuss alternative inputs for your portfolio optimization problem.

2. **Expected risk and return based on historic data**
Efficient frontier optimization requires knowledge of the expected risk Sigma and expected returns mu. In practice, these are rather difficult to know with any certainty. The best we can do is to come up with estimates, for example by extrapolating historical data. But that is where we go wrong. If history would repeat itself perfectly, we would all be able to predict financial markets and stock movements. The truth is, the mean historic returns, or the historic portfolio variance are not perfect inputs and do not reflect future expected risk and return perfectly. Hence the resulting weights of our optimization problem, would have worked well in the past, but we have no guarantee that it will work well in the future.

3. **Historic data**
This graph illustrates the problem well. If you were to take the mean of the first data points, and use that to predict the mean at end of the time series, your prediction would be totally wrong.

4. **Exponentially weighted returns**
So what can we do about this? Well, the problem is not with the optimization approach; that procedure is sound, and provides strong mathematical guarantees, given that the inputs are correct. We therefore need to think about better measures for expected risk and return. A possible improvement is to use exponentially weighted risk and return. It assigns more importance to the most recent data, and thus aims to improve the estimates. Here you see how an exponential mean, or moving average, is build up. The last observation at t-1 gets assigned the heaviest weight in the mean.

5. **Exponentially weighted covariance**
You can do the same for volatility. The exponential covariance matrix also gives more weight to recent data when calculating covariance, in the same way that the exponential moving average is calculated. In the graph you see how the exponential weighted volatility in black, follows the actual volatility depicted in the upper part of the graph, much better than the standard volatility in blue.

1 Source: https://systematicinvestor.github.io/Exponentially-Weighted-Volatility-RCPP

6. **Exponentially weighted returns**
Let's see how you can adjust your code to use exponentially weighted risk and return in the optimization problem. The adjustments happens where you define mu and Sigma. The expected return function has the exponentially weighted return as an option, so let's use that. Then let's define a span which is the look back window over which you calculate the return. Also define a frequency, which is simply the number of trading days in a year. The output is simply the exponentially weighted mean for each stock in your portfolio.

7. **Exponentially weighted covariance**
The exponentially weighted covariance is also just another option in the risk_models function. For Sigma, you therefore follow the same steps. Take the exponential_cov from the risk models function, define the span and keep the frequency to 252 trading days. I take a different span for the variance calculation here, as it does not need to be the same span as for the exponential returns calculation.

8. **Using downside risk in the optimization**
Another way to adjust our portfolio optimization problem, is to use downside risk only. Remember what we did for the Sortino ratio? For that ratio you calculated the variance of the negative returns only, as a way to measure downside risk. In PyPortfolioOpt you can do the same, but here it is called semicovariance. So instead of using the standard volatility, you can use the semicovariance matrix for the portfolio optimization problem.

9. **Semicovariance in PyPortfolioOpt**
Making the adjustment to use the semicovariance for risk, is again very straight forward. Simply take the semicovariance option from risk models, at the point where you define Sigma. In this case, you need to define a benchmark, if the return falls below this benchmark it's considered a negative return and used in the variance calculation. Let's go with zero for this case. Define the frequency also, which is the number of trading days. You see that the semicovariance looks just like a normal covariance matrix, however it's calculated on the negative returns only.

10. **Let's practice!**
Let's practice!