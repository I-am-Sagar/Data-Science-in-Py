1. **Maximum Sharpe vs. minimum volatility**
In this video, we're going to dive deeper into the differences between the maximum Sharpe and the minimum volatility portfolios.

2. **Remember the Efficient Frontier?**
In the last video we covered the efficient frontier, which contains all possible portfolios with optimal risk and return trade-offs. We now want to look at two special cases on the efficient frontier, the Maximum Sharpe portfolio and the minimum volatility portfolio. The Maximum Sharpe is a special case on the efficient frontier. Of all the risk-return optimized portfolios, it has the highest Sharpe ratio. The minimum volatility is also a special case, as it is the one portfolio on the efficient frontier with the lowest level of risk.

3. **Adjusting PyPortfolioOpt optimization**
Luckily, PyPortfolioOpt can obtain those two special cases for you. As you see in this picture, PyPortfolioOpt can combine the expected returns and the risk measure and calculate four different types of optimized portfolios. The maximum Sharpe, the minimum volatility, and lastly the efficient risk and return portfolios, which you saw in the last video.

4. **Maximum Sharpe portfolio**
Most portfolio managers are interested in finding the Maximum Sharpe portfolio on the efficient frontier, when they do their portfolio optimization. Let's calculate it with PyportfolioOpt. Import the efficient frontier function again, and feed it your expected returns and covariance matrix. Then, use max_sharpe() to obtain the maximum Sharpe ratio portfolio, and store those portfolio weights to raw_weights. Then, because the raw weights are the direct output of the optimization problem and difficult to read, you collect the clean weights which look tidy and better understandable.

5. **Maximum Sharpe portfolio**
Last, you can get the performance numbers by running portfolio_performance on ef. As you can see, it returns the annualized return number and annualized volatility, as well as the Sharpe Ratio, so you don't have to calculate those again.

6. **Minimum Volatility Portfolio**
The minimum volatility portfolio gives you the most optimal portfolio for the least amount of risk. It's in that sense a special case, as it serves as the "lowest risk benchmark" to all other portfolios on the efficient frontier. It does perform surprisingly well over time, and therefore some managers choose this portfolio as their preferred portfolio. Calculating it is very easy with PyPortfolioOpt. Get the efficient frontier using mu and Sigma. Then, this is where things change: use min_volatility as the optimizer. The rest of the steps are the same; you can get the clean weights like this...

7. **Minimum Volatility Portfolio**
And here are the performance numbers. There you have it, the minimum volatility portfolio. Notice that it typically will have lower performance, and a lower return, and for obvious reasons, a lower Sharpe ratio than the maximum Sharpe portfolio.

8. **Let's have another look at the Efficient Frontier**
Now let's look again at this graph. Remember risk is located on the x-axis, and returns are on the y-axis. Where do you think the minimum volatility portfolio lies? It's one of the stars on the efficient frontier. And which of the stars is the maximum Sharpe portfolio? What's your guess?

9. **Maximum Sharpe versus Minimum Volatility**
The minimum volatility portfolio is the blue star. It has the lowest risk possible, so it's always on the left of the maximum Sharpe portfolio. The maximum Sharpe portfolio is higher on the efficient frontier, as it will have a higher volatility by definition.

10. **Let's practice!**