1. **Volatility and extreme values**
Structural breaks in volatility are often a sign of extreme events, another important consideration in the risk management landscape.

2. **Chow test assumptions**
The Chow Test is a very useful way to identify whether or not a structural break has occurred. The test requires both knowledge of where a structural break has occurred, and a linear model (such as the Fama-French factor model we discussed in Chapter 1).

3. **Structural break indications**
Visually identifying the exact moment of a structural break is often not possible, due to noise in the data. The trend of the data may not reveal a distribution change. One way to address this is to examine if times of structural change coincide with times of increased volatility. After all, change is often accompanied by greater uncertainty about the future, and this translates into more volatility. Examining volatility also allows for a richer class of risk factor models to be applied and tested, such as the stochastic volatility models commonly used in asset pricing.

4. **Rolling window volatility**
We can see if volatility is non-stationary by constructing a rolling window of losses (or returns) and computing the volatility for each window. Recall that we can compute a rolling window from Pandas DataFrame and Series objects using the `rolling()' method, find the rolling window volatility, and then compute statistics such as the mean, minimum or maximum, and others.

5. **Rolling window volatility**
Plotting the resulting volatility series can help identify dates where the volatility appeared to change significantly. These can then be used with the Chow Test to see if one or more structural breaks is supported by the data.

6. **Rolling window volatility**
It is sometimes also helpful to visualize changes in volatility, rather than volatility itself. This provides, in addition to possible structural break points, useful information about how the variance has changed over time. Such changes can often be modeled as time-varying volatility. Linear models can be tested with a variant of the Chow test if this is the case. In addition, allowing time-varying volatility introduces richer models such as the popular autoregressive conditional heteroskedasticity or ARCH models, as well as the previously mentioned stochastic volatility models.

7. **Extreme values**
A second method of identifying structural breaks uses the same concepts as VaR and CVaR. Recall that VaR finds the maximum loss for a particular confidence level. Plotting this maximum loss can indicate a point where the trend in the VaR changes. If there is a lot of data, so that computing the quantile for the VaR over time is feasible, then this is a useful approach. But smaller datasets may not provide enough information to visualize the VaR over time. As an alternative, we can examine points in time where losses simply exceed some threshold. For example, a 95% VaR estimate means that, in real-world data, losses should exceed the estimate 5% of the time. If we examine previous data and see how often losses exceed the VaR estimate, then we are performing backtesting on the VaR threshold. Backtesting is an important performance indicator of a measured risk estimate such as VaR and CVaR, and is used extensively in enterprise risk management.

8. **Backtesting**
Suppose we would like to understand the risk that daily losses exceed 3%, which is a 95% VaR estimate we obtained from an earlier estimation procedure. This a large change in the relative portfolio value in the single day, making such losses an "extreme value". By backtesting, we would expect that around 5% of historical losses will exceed our VaR estimate. Any more, and we have an underlying distribution in the past with wider distribution tails than that assumed when deriving the VaR estimate. Any less, and we have an historical distribution with narrower tails than that used for the estimate. It's important to emphasize that any loss threshold can be used for backtesting. In particular, the CVaR is widely used for backtesting because it explicitly takes into account the tail of the loss distribution.

9. **Let's practice!**
In the exercises you’ll use both volatility and extreme value visualizations to identify possible structural breaks during the global financial crisis.

