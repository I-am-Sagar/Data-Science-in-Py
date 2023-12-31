1. **Strategy optimization and benchmarking**
Welcome back!

2. **How to decide the values of input parameters?**
In previous lessons, we have built and backtested several trading strategies. But when implementing a strategy, how do we determine the values of input parameters? For example, when we construct the signal based on the price and SMA comparison, what is the SMA lookback period we should use? Can a 10, 20, or 50-period SMA result in a more profitable strategy? The solution is to conduct strategy optimization, which is the process of testing a range of input parameter values to find the ones that give better strategy performance based on historical data.

3. **Strategy optimization example**
Let's look at an example of performing strategy optimization. In lesson 1 of this chapter, we implemented a strategy based on a price and SMA comparison. To find the SMA lookback period that can optimize the strategy performance, we want to run multiple backtests by varying the SMA timeperiod parameters on different runs. To make the code reusable, we will define a Python function. A function is a block of reusable code which runs when it is called. You can pass data into a function. A function can also return data as a result. If you are interested in learning more about it, check out DataCamp's course. Here we define a function signal_strategy that packages the process of implementing the strategy. After def signal strategy, we can pass a number of parameters in a function header that our function will accept. We can pass the period as a parameter to change the SMA lookback period. In addition, we can pass the stock ticker, start date, and end date to run backtests on different stocks and on different historical periods. Note that by specifying a value of a parameter in the header, we set a default argument that will be used if an argument is not passed. For example, here we set the start and end parameters with default dates. Within the body of the function, our code can then use the values these parameters take when the function is called. Lastly, we use the return keyword to return the backtest whenever the function is called.

1 www.datacamp.com/courses/writing-functions-in-python

4. **Strategy optimization example**
Then we can call the function several times to pass different SMA lookback parameters. Each function will return a bt Backtest. Call bt dot run to run all the Backtests at once, and plot the results in one chart for easy comparison. From the chart we can see using the 20-period SMA gives us the most profitable strategy based on the historical period backtested.

5. **What is a benchmark?**
A benchmark is a standard or point of reference against which a strategy can be compared or assessed. For example, a strategy that uses signals to actively trade stocks can use a passive buy and hold strategy as a benchmark. A benchmark can also be chosen based on the market segments and asset risk profiles. For example, the S&P 500 index is often used as a benchmark for US equity performance, and US Treasuries are used for measuring bond risks and returns.

6. **Benchmarking example**
Continue the previous example, let's define a benchmark. Instead of using a signal-based strategy to actively trade a stock, we will passively hold the stock and use its performance as the benchmark. Define a separate function to describe the benchmark. Use bt algos RunOnce to implement a passive strategy, that is buy a stock at the beginning of the period and just hold until the end of the period.

7. **Benchmarking example**
Then call the function to create a bt Backtest. Similarly, we can use bt dot run to run multiple backtests and plot their results together. The results look interesting. They suggest some active strategies outperformed the benchmark whereas some underperformed.

8. **Let's practice!**
Fantastic! Now it's your turn to practice!