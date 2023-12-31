1. **Markowitz portfolios**
Now that you've nailed down the fundamentals of correlation and co-variance, it's time to see how we can use them to build superior portfolios.

2. **100,000 randomly generated portfolios**
Imagine you have 9 assets, and have randomly generated 100 thousand different portfolio examples, each with different weights, and different levels of risk and return. Which one is best?

3. **Sharpe ratio**
In order to compare portfolio performance, you'll want to take into account risk-adjusted returns. The Sharpe ratio is a useful metric which is quoted quite frequently in finance for this purpose. The Sharpe ratio measures how much return an investor can be expect for each incremental unit of risk, and thus can be used to compare portfolios with different levels of risk. This formula assumes a risk-free rate of return, but for this chapter we can assume that this value is 0.

4. **The efficient frontier**
According to modern portfolio theory, pioneered by Harry Markowitz in 1952, there is an efficient frontier of portfolios, each with the highest expected return for a given level of risk. This is essentially the portfolios on the top left edge when plotted with risk on the x-axis and expected return on the y-axis. You can select the tangency portfolio, which is the portfolio with the highest Sharpe ratio, and crosses the capital allocation line according to the CAPM theory. We'll talk more about CAPM in the next chapter. The tangency portfolio is known as the max sharpe ratio, or MSR portfolio.

5. **The Markowitz portfolios**
The GMV, or global minimum volatility portfolio, is the portfolio on the far laft edge of the plot with the lowest volatility. Both the MSR and GMV are known as Markowitz portfolios. The closer you are to the efficient frontier, the green line, the better the portfolio. Now, you can't see it on this chart, but where the capital allocation line hits 0 on the x-axis, that would be the risk free rate.

6. **Choosing a portfolio**
Note that any portfolio below the efficient frontier is technically sub-par when compared to other possible portfolios. Choosing a point on the efficient frontier is a matter of personal preference. High return is available at the cost of higher risk.

7. **Selecting the MSR in Python**
You will now be given a list of randomly generated portfolios with their risk and return figures. In order to select the MSR, or max Sharpe ratio portfolio, you will first need to calculate the Sharpe ratio for each portfolio in the dataset. You can do this by first subtracting the risk free rate from the returns, and then dividing by the volatility column. In this case, we assume that the risk free rate is 0, so it doesn't matter, but we'll keep it in the formula just in case interest rates shoot up in the future and we need to incorporate them into our analysis. Next, sort the DataFrame by Sharpe ratios using the dot-sort_values() method with ascending = False to get the top Sharpe ratio portfolios. Finally, you can use the dot-iloc accessor to only select the first 5 weight columns if you only have a portfolio with 5 assets.

8. **Past performance is not a guarantee of future returns**
Now keep in mind that historical Sharpe ratios aren't an indication of future performance. In fact, Sharpe ratios change quite dramatically over time.

9. **Selecting the GMV in Python**
You can find the GMV, or global minimum volatility portfolio by sorting by the Volatility column instead, but this time with ascending equals True to select the portfolio with the lowest volatility. The global minimum volatility portfolio actually tends to do pretty well over time, whereas the MSR portfolio tends to be rather inconsistent.

10. **Let's practice!**
Now it's your turn to build some portfolios!