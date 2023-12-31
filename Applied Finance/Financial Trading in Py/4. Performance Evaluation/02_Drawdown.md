1. **Drawdown**
In this lesson, let's learn about a performance evaluation metric called drawdown.

2. **What is a drawdown?**
A drawdown is a peak-to-trough decline during a specific period for an asset or a trading account. A drawdown is usually quoted as the percentage between the peak and the subsequent trough. If a trading account has 1000 in it, and the fund drops to 900 before moving back above 1000, then the trading account has experienced a 10% drawdown. Drawdowns are a measure of downside volatility.

3. **Max drawdown**
A max drawdown is the maximum observed loss from a peak to a trough of an account, before a new peak is established. Max drawdown is an indicator of downside risk over a specified time period. For example, if an account begins with a value of 1000, increases in value to 1700 (point A), decreases to 900 (point B), increases to 1400 (point C), then decreases to 800 (point D), then increases to 2000 (point E), the max drawdown is 1700 (at point A) minus 800 (at point D) then divided by 1700, or about 53%.

4. **Obtain drawdowns from backtest stats**
We can get various types of drawdown results, such as max drawdown, average drawdown, and average drawdown days from the stats DataFrame as the sample code demonstrates. The average drawdown is the mean drawdown percentage during the strategy backtest period, and the average drawdown days equals the number of days on average that the portfolio or account would remain in a drawdown period.

5. **The Calmar ratio**
The Calmar ratio was created by a hedge fund manager named Terry Young and first published in 1991. The name Calmar is an acronym of Young's company name and its newsletter: California Managed Accounts Report. Calmar ratio is calculated as a portfolio or account's compounded annual growth rate, or CAGR, divided by its max drawdown. People also refer to the Calmar ratio as the drawdown ratio. Since the max drawdown is a measure of downside risk, the higher the Calmar ratio, the better a strategy performed on a risk-adjusted basis during the given timeframe. As a rule of thumb a Calmar ratio larger than 3 is considered excellent.

6. **Calculate the Calmar ratio manually**
We can calculate the Calmar ratio manually using stats from the backtest result. As the sample code demonstrates, the Calmar ratio equals the CAGR divided by the max drawdown, both are available by slicing the stats DataFrame. Doing so can give us an intuitive understanding of how the Calmar ratio is obtained. Also note the max drawdown is multiplied by minus 1 during the calculation to convert the result to a positive number. It is formatted to print a float number with 2 decimal points.

7. **Obtain the Calmar ratio from backtest stats**
We can also get the Calmar ratio directly from the backtest result stats by referring to the name calmar.

8. **Let's practice!**
Excellent! Now let's practice!