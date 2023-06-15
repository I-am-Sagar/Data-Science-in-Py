1. **Modern portfolio theory**
Now that we understand risk factors, we can better understand the relationship between risk and return.

2. **The risk-return trade-off**
It makes intuitive sense that the greater our appetite for risk, the greater should be our expected future return. After all, we expect to get something more by assuming more risk! But we cannot generally guarantee a return: we can only speak about an expectation. One expected return measure often used is the average (mean) historical return over time. This is a proxy for future returns.

3. **Investor risk appetite**
Imagine that we conduct a survey, asking investors what their expected minimum return needs to be, for them to assume a certain level of risk. Their answer is one “data point” of an investor’s risk profile. Asking the same question many times, with a different level of risk each time, creates a list of (risk, expected minimum return) points. These points give us information about the investor’s "risk appetite".

4. **Choosing portfolio weights**
Instead of answering a survey, an investor can achieve a (risk, return) pair for a portfolio by adjusting the portfolio's weights. This is our first step toward risk management! An investor wants the highest expected return for a given level of risk. Alternatively, we could vary the weights to find the smallest level of risk for a given expected return. In either case, we are performing risk management: changing the portfolio's weights changes an investor's risk exposure to achieve a (risk, return) combination that respects the investor's risk appetite.

5. **Modern portfolio theory**
A portfolio with weights providing the highest expected return for a given risk level is called an “efficient portfolio”. This mathematical way of quantifying the risk-return trade-off is called “Modern Portfolio Theory”, created by Nobel Laureate H M Markowitz in the early 1950s. The efficient portfolio is the solution to an optimization problem, which selects portfolio weights to maximize the expected portfolio return, conditional upon a particular risk level given by the portfolio's volatility.

6. **The efficient frontier**
Just as in our risk appetite example, we can compute the efficient portfolio across a wide range of risk levels. This will again give us a set of (risk, return) pairs, and these can be plotted to create the “efficient frontier”. We can use the PyPortfolioOpt library to compute the efficient frontier. The standard way to do this is to create an EfficientFrontier object. But this only finds one optimal portfolio and not the entire frontier. Instead, we'll use a Constrained Line Algorithm, or CLA, which can generate the efficient frontier. We need both the covariance matrix and also our proxy for the expected return, the mean historical return.

7. **Investment bank portfolio 2005 - 2010**
We can use PyPortfolioOpt on our investment bank portfolio to find and visualize the efficient frontier for the period 2005 - 2010. To do this, we first compute the expected return using historical asset price data. Then we derive an efficient estimate of the covariance matrix, using the CovarianceShrinkage object. This improves the sample covariance by "shrinking" extreme errors that can be caused by sampling. We use the popular Ledoit-Wolf method here to compute the efficient covariance matrix. Using these we create the CLA object. Remember, this object allows us to plot the entire efficient frontier. Next we find the minimum variance portfolio using the .min_volatility() method, which will be discussed shortly, and finally the efficient frontier with the .efficient_frontier() method. This provides, in addition to portfolio weights, risk and return values within the 'vol' and 'ret' variables, respectively.

8. **Visualizing the efficient frontier**
We can create a visual representation of the efficient frontier by plotting the resulting efficient portfolio pairs.

9. **Visualizing the efficient frontier**
Notice that in the plot of the efficient frontier, one portfolio stands out as having the smallest volatility possible: this is the minimum variance portfolio, and is often used as a benchmark to assess an investor’s risk appetite.

10. **Visualizing the efficient frontier**
An investor may wish to assume more risk (higher volatility), which carries a higher expected return. They move along the efficient frontier until they find an efficient portfolio that matches their risk appetite.

11. **Let's practice!**
In the exercises to follow you’ll practice using PyPortfolioOpt, and break up the 2005 -2010 period into time periods before, during and after the financial crisis, examining the efficient frontier for each period. Good luck!

