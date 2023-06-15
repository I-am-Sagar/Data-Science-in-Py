1. **Risk management using VaR & CVaR**
Now that we can measure how much a portfolio stands to lose, we can mitigate this risk in a similar fashion to the efficient portfolio. Let's see how this works in practice!

2. **Risk management via modern portfolio theory**
In Chapter 1 we introduced the efficient portfolio, derived by finding optimal portfolio weights that maximize the expected portfolio return given a particular level of risk. By performing this procedure over and over again for different levels of risk, we created the efficient frontier. Finding the efficient portfolio and frontier was performed using Modern Portfolio Theory, our first tool for portfolio risk management.

3. **Incorporating Value at Risk into MPT**
Modern portfolio theory is also called mean-variance portfolio optimization because it asks for the highest expected return, given our level of risk expressed as a variance. The expected return is the objective function of the optimization problem. By contrast, the VaR and CVaR risk measures address how much we expect to lose and not just a particular risk level. We can adapt modern portfolio theory to optimize over loss distributions.

4. **A new objective: minimize CVaR**
We do this by changing the objective function of the optimization problem: that is, instead of looking for the portfolio weights that maximize the expected portfolio return, we look for the portfolio weights that minimize the expected conditional loss at some confidence level. In other words, we minimize the CVaR. For example, given a VaR loss with 95% confidence, we would optimize portfolio weights to find the minimized CVaR, conditional upon the VaR. That is, we would find the portfolio that has the lowest expected loss in the worst 5% outcomes, i e at the 95% VaR level of confidence.

5. **The risk management problem**
This optimization problem selects optimal portfolio weights 'w-star' to minimize the CVaR, given a confidence level 'alpha'. Remember that here 'x' is the portfolio loss, and depends upon the weights 'w'. Loss is the negative of returns, and its distribution 'f(x)' is calculated from a numerical estimate (we'll examine how to do this in Chapter 3). As always the portfolio weights have to sum up to one. We can use PyPortfolioOpt to perform this minimization by selecting CVaR as a new objective function.

6. **CVaR minimization using PyPortfolioOpt**
To minimize CVaR, we first create an 'EfficientCVaR' object. We only pass in asset returns since we won’t maximize expected return. Then we use the EfficientCVaR’s `min_cvar()' method to find the minimized CVaR portfolio.

7. **Mean-variance vs. CVaR risk management**
We can compare the minimum CVaR portfolio to the minimum volatility mean-variance solution for the 2005 - 2010 investment bank portfolio. We compute the minimum volatility portfolio weights in the usual fashion, by creating an EfficientFrontier instance and using the 'min volatility' method. As we see, the minimum variance portfolio advises holding only Goldman Sachs and J P Morgan, to minimize volatility over the period.

8. **Mean-variance vs. CVaR risk management**
By contrast, the CVaR-minimizing portfolio is created using the 'EfficientCVaR' object and its `min_cvar()' method, as described earlier. The result is a portfolio heavy in Goldman Sachs and J P Morgan. This creates more volatility than the minimum volatility mean-variance portfolio, but with the benefit that the worst 5% cases of loss are minimized.

9. **Let's practice!**
Risk management using Conditional Value at Risk minimization is an important step forward. Now you can apply this technique to the global financial crisis!

