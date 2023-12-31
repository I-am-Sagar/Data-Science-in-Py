1. **Sharpe ratio and Sortino ratio**
In this lesson, we will learn two more useful concepts to measure strategy performance.

2. **Which strategy performs better?**
Think for a second: in terms of return, is bigger always better? Suppose we have two strategies with the following results. Strategy 1 has a 15% return and 30% volatility, measured by the return standard deviation. Strategy 2 has a 10% return and 8% volatility. Which strategy do you think has better performance? Remember your pick and we return to this later.

3. **Risk-adjusted return**
To make performance comparable among different strategies, we should take both return and risk into consideration. Hence, risk-adjusted return is a ratio introduced to assess a strategy performance by measuring how much risk is involved in producing a certain level of return. In this context, is a bigger return always better? Not necessarily. For example, a 20% return is impressive. But if it comes with a return volatility of 40% due to trading speculative or risky assets, the performance is actually moderate from a risk-adjusted perspective.

4. **Sharpe ratio**
One risk-adjusted return measure is called the Sharpe ratio, developed by Nobel Laureate William F.Sharpe. The Sharpe ratio is calculated as the average return in excess of the risk-free rate, divided by the excess return volatility, ie standard deviation. The risk-free rate is usually the equivalent of a safe risk-free bond, such as US Treasuries or UK Gilts. Under the current low interest rate or even negative interest rate environment in the US and Europe, we can assume the risk-free rate to be zero. The Shape ratio provides a simple way to measure return obtained per unit of risk. In general, the bigger the Sharpe ratio, the more attractive the risk-adjusted return.

5. **Now choose again**
Now let's return to the previous question. Given the information we can calculate the Sharpe ratio for each strategy. Strategy 1 has a Sharpe ratio of point 5 and strategy 2 has 1 point 25. Clearly, strategy 2 performs better since it generates 1 point 25 units of excess return per unit of risk, compared to only point 5 of strategy 1.

6. **Obtain Sharpe ratio from bt backtest**
To obtain the Sharpe ratio from bt backtest result, first call dot stats to obtain all backtest statistics and save them in a DataFrame. Then we can get the Sharpe ratio by slicing the DataFrame. There are daily, monthly and yearly Sharpe ratios available from the stats. In addition, we formatted the output to print a float with two decimals places.

7. **Calculate Sharpe ratio manually**
We can also calculate the Sharpe ratio using the annual return and volatility from the stats manually as shown in the code. This calculation enables us to see each component of the Sharpe ratio.

8. **Limitations of Sharpe ratio**
Despite the benefits afforded by its simplicity, the Sharpe ratio is criticized for using the total return volatility in the calculation. In other words, it does not distinguish good/upside volatility from bad/downside volatility, and punishes both equally. In reality, upside volatility, although desirable, can skew the results downward, resulting in a lower Sharpe ratio. It hence paints an inaccurate picture of the risk-reward efficiency.

9. **Sortino ratio**
To address this deficiency, the Sortino ratio is a modification of the Sharpe ratio. Instead of using total volatility, the return in excess of the risk-free rate is divided by the downside volatility, or downside deviation of the return. In other words, only the downside risk will be punished.

10. **Obtain Sortino ratio from bt backtest**
We can obtain the Sortino ratio from the backtest statistics in a similar way as the Sharpe ratio. There are daily, monthly, and yearly Sortino ratios available. The bigger the Sortino ratio, the better the performance.

11. **Let's practice!**
Now it's your turn!