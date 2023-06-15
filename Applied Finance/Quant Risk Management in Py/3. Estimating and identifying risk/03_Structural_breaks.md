1. **Structural breaks**
We'll now investigate how structural changes affect our measurement and estimation of risk in real data.

2. **Risk and distribution**
Up to now our main tool for risk mitigation is Modern Portfolio Theory, while our main measurement tools are Value at Risk and Conditional Value at Risk. We have identified risk with dispersion or volatility of risk factors, giving us statistical variance as a quantitative measure. In turn, this provides a connection between risk and an underlying statistical distribution that risk factors are assumed to follow.

3. **Stationarity**
This connection also assumes that the underlying distribution is the same over the time the risk factor data is collected. In other words, the loss (or returns) distribution is stationary. But as we saw in Chapter 1, the efficient frontier was different depending upon which part of the global financial crisis period was studied. So it may be the case that the distribution of losses is not stationary. This poses a problem for our estimation of risk, because all three estimation procedures we discussed in the last video (historical, parametric, and Monte Carlo) assume stationary distributions.

4. **Structural breaks**
If we knew that the distribution was changing over time, and we knew when distribution changes occur, then we could estimate our risk measures only during sub-periods when the distribution didn't change. In other words, distributions would be stationary only within certain sub-periods of the data. We first need to know when the data suggest that an underlying distribution is changing. This is the known as a "structural break" point in the data. You can think of a structural break as a change in a “trend”.

5. **Example: China's population growth**
As an example of a structural break, let's examine the population growth rate of China from 1950 to 2019. We can see that the growth is relatively linear over this period,

6. **Example: China's population growth**
but around 1990 the growth rate slows down. This indicates that there may be a structural break around 1990. In other words, the underlying distribution of net population gains (births minus deaths) changed, causing there to be fewer net gains from 1990 onwards. Some reasons for such a change could be changes in government policy, changes in living standards, and other micro- and macro-level factors.

7. **The Chow test**
A visual examination is useful to identify structural breaks. But there are also powerful statistical tools that can be applied to data. One tool is the “Chow Test”, which asks if the data support a structural break at a given break point of time, for a given linear risk factor model. Its null hypothesis is no structural break. In the test, three ordinary least squares regressions are performed: one for the entire period, and two for before and after the break point. The sum-of-squared residuals are then collected, and the Chow test statistic is created. The statistic is distributed as an "F"-distribution statistic.

8. **The Chow test in Python**
Let's use the Chow test to see if there was a structural break somewhere around 1990 in China's population growth. We'll use a very simple "factor model" where log-population is regressed against year. First we perform an OLS regression over the 1950 - 2019 period, regressing the natural logarithm of population against year and an intercept. This gives our 'baseline' regression, assuming no structural break. The sum-of-squared residuals from the regression are stored.

9. **The Chow test in Python**
Then we break the time period into two sub-periods: 1950 - 1989 and 1990 - 2019, and run regressions for each sub-period. We then store the sum of squared residuals for both regressions.

10. **The Chow test in Python**
Finally, we compute the Chow test statistic using the three sum of squared residuals and the degrees of freedom of the test. The Chow test statistic should be distributed as an "F" distribution. The "F" distribution has two degrees of freedom: the first (used in the numerator) is the number of regression parameters, here equal to 2: the intercept and slope coefficient. The second (used in the denominator), is the total number of data points, 70, minus twice the first degree of freedom, or 70 minus 4, which is 66. The computed test statistic is statistically different from zero at the 99-point-9% confidence level. We can reject the null hypothesis that there was no structural break in the data.

11. **Let's practice!**
Now you’ll apply the Chow test to identify a possible structural break in the investment bank portfolio data during the global financial crisis.

