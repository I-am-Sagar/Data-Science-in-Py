1. **Estimating tail risk**
A key component of portfolio risk management is being able to define risk beyond simple measures such as standard deviation, variance, and even kurtosis. More important is the ability to quantify potential losses on a single stock and portfolio level.

2. **Estimating tail risk**
Tail risk is essentially the risk of extreme outcomes in the tail of the return distribution, particularly in the left tail, which signifies an extremely negative return. In this chapter, you'll cover multiple methods of estimating tail risk including historical drawdowns, two different methods for value at risk and conditional value at risk, and finally - Monte Carlo simulation.

3. **Historical drawdown**
Historical drawdown is a way to estimate the percentage loss from the highest point. In other words, how far have you fallen from your best point in history? Great investments would ideally have little to no drawdown since they would simply be growing consistently over time, but in reality you can expect drawdowns to happen quite frequently in most portfolios.

4. **Historical drawdown in Python**
Given the formula from the previous slide, it is relatively simple to calculate historical drawdown in Python by using the maximum and accumulate functions to calculate the running maximum over time, which is essential to the formula. First, call np dot maximum dot accumulate on your cumulative returns to get your running maximum over time. But you're only interested in losses, so next, set the running maximum to be upper-bounded by 1, which is your starting point. Finally, divide the cumulative returns by the running maximum, and subtracting 1 to center the series at 0. This is your drawdown, and as you can see, it will never rise above 0.

5. **Historical Value at Risk**
Value at risk, often referred to as VaR, is a way to estimate the risk of a single day negative price movement. VaR always has a quantile, or percentage attached to it. For example, a VaR 95 of -2-point-3% means in the worst 5% of scenarios, my losses will exceed -2-point-3%. You can think of it the other way around - I can be 95% certain that my losses will not exceed -2-point-3% in a given day.

6. **Historical Value at Risk in Python**
You can use the np dot percentile function to easily calculate the 95 percent quantile of a distribution. But in this example, you want to pass 100 minus 95, which is just 5. If you wanted the 90th percentile, you would pass 100 minus 90, which is 10. Just note that this function expects integers instead of decimals, for example 10 instead of 0.10.

7. **Historical expected shortfall**
Conditional Value at Risk, otherwise known as CVaR, is a measure of the expected value of losses in the worst 1 minus x percent of scenarios, which is where the alternative name "expected shortfall" is derived from. In this example, CVaR(95) = -2-point-5 percent means that in the worst 100 - 95, or the worst 5 percent of cases, losses will be on average -2-point-5 percent. This is essentially the same as taking the average of losses exceeding the VaR(95) level. Just like VaR, CVaR 95, 99, and 99-point-9 are common.

8. **Historical expected shortfall in Python**
For example, in Python, you can simply compute VaR(95) as before, and then subset the returns, taking the mean of all returns less than or equal to the VaR(95). This means that your CVaR will always be worse than your VaR of the same quantile.

9. **Let's practice!**
Ready to try it out?