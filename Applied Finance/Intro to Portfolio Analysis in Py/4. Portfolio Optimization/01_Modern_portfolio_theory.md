1. **Modern portfolio theory**
Let's now dive into portfolio optimization.

2. **Creating optimal portfolios**
So far we have analyzed risk, return and factor exposures of portfolios, but we haven't discussed how to create a portfolio. How do you devise an investment strategy, that gives you your desired risk and return trade-off, or simply put: which assets are you going to put in your portfolio? That's what we're going to discuss in this chapter.

3. **What is Portfolio Optimization?**
Thankfully, there are existing models you can use, to help you select stocks for your portfolio. Harry Markowitz came up with Efficient Frontier Optimization in 1952, which provides a solid framework for combining stocks in a portfolio. The key insight is that by combining assets with different expected returns and volatilities, one can decide on a mathematically optimal allocation.

4. **The optimization problem: finding optimal weights**
The Efficient Frontier Optimization is a constrained optimization problem, in which you try to minimize portfolio variance by setting the weights. The top line should look familiar to you, it's something you've calculated many times in Chapter 1, and it is in fact the portfolio variance! Do you recognize it? It's weights transposed, times the covariance matrix sigma, times the weights again. The "subject to" conditions simply state that the expected return, or weights times mu, should be at least some target level of return, mu star. Then, it says that the weights should some up to 1, and that at least some of the weights should be positive.

5. **Varying target returns leads to the Efficient Frontier**
When you change the target return mu star in the optimization problem, the weights w that form the optimal solution, change. So in fact, the solution to the Markowitz' optimization problem, is a collection of portfolios, which we call the efficient frontier. The line in the graph represents that frontier. The dots are individual portfolios plotted with their respective risk and return profile. The efficient frontier is thus the set of optimal portfolios that offers lowest risk for a given level of expected return and visa versa.

6. **PyPortfolioOpt for portfolio optimization**
PyPortfolioOpt is an incredibly useful library to help you find optimal portfolios. So no need to create and solve an optimization problem yourself. Let's start by importing the package and the functions we need. The expected_return and risk_models functions need the daily price data as input, so let's take this set of stocks and their prices over time. Then, let's take the mean historical return to calculate expected return for the portfolio. Finally, we use the sample covariance function to get a measure of risk.

7. **Get the Efficient Frontier and portfolio weights**
Having calculated the expected return mu and risk sigma from the price dataset df, you are now ready to calculate the efficient frontier, which you can create with just one line of code. Ef now contains all the risk and return optimized portfolio, and you can just pull specific cases out of it, in this case let's take the maximum Sharpe ratio portfolio, and grab the weights such that we can see what it looks like.

8. **Different optimizations**
From the efficient frontier we can actually select multiple portfolios. You saw we can get a portfolio that maximizes the Sharpe ratio, but with efficient_risk() you get the maximum return portfolio for a given target risk in brackets, and visa versa with efficient_return() you select the portfolio that minimizes the risk for that given target return.

9. **Calculate portfolio risk and performance**
Last, you can very easily obtain the optimal portfolio performance numbers with this command. This gives you the expected risk and return, as well as the Sharpe ratio. The verbose = True option just makes sure the performance numbers are printed after the function, the default is False, in which case the numbers are not printed. You can also set the risk free rate, which defaults to 0.02 if not adjusted.

10. **Let's optimize a portfolio!**
Let's optimize a portfolio!