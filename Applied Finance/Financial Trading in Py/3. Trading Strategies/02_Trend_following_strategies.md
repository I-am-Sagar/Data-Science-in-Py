1. **Trend-following strategies**
Let's build and backtest a trend-following strategy!

2. **Two types of trading strategies**
The two most popular types of trading strategies are trend following and mean reversion. Trend following, also known as a momentum strategy, bets that the price trend will continue in the same direction. You implemented a simple trend-following strategy in the previous lesson. When the price rises above its moving average, enter a long position to bet the price will continue to rise. Traders commonly use trend indicators such as moving averages, ADX, etc to construct trading signals for trend following strategies. Mean reversion strategies, conversely, bet that when the market reaches an overbought or oversold condition, the price tends to reverse back towards the mean. We will learn more about them in the following lesson. Traders commonly use indicators such as RSI, Bollinger Bands, etc, to construct trading signals for mean-reversion strategies. Markets are constantly moving in and out of phases of trending and mean reversion. Therefore it's beneficial to develop strategies for both phases.

3. **MA crossover strategy**
The philosophy of trend following strategy is: the trend is your friend. Let's look at a common example of a trend-following strategy called MA crossover, which involves two moving average indicators, one longer and one shorter. We will use the EMA for example. When the short-term EMA crosses above the long-term EMA, it is a long signal, as it suggests the price is picking up momentum. When the short-term EMA crosses below the long-term EMA, it's a short signal, as it suggests that the price is losing momentum.

4. **Calculate the indicators**
First, let's calculate the indicators with the talib EMA function. Note we use to underscore frame to save the result as a pandas DataFrame.

5. **Construct the signal**
We construct the signal by copying the EMA indicator DataFrame with the dot copy method. We set the signal value to 0 for the initial n periods that do not have enough data points for the EMA. Then, we define the signal. When the short-term EMA value is larger than the long-term EMA value, the signal is one indicating a long position; when short-term EMA is smaller than the long-term EMA, the signal is minus one indicating a short position. Note that shorting a stock essentially means betting the price will go down, and entails selling borrowed shares, and later buying them back at market price.

6. **Plot the signal**
We can plot the signal with the price and EMA indicators together. First use bt merge to combine multiple DataFrames. It takes in several DataFrames and merges them into one based on the DataFrame index, in this case the Date. Then use the dot columns attribute of the DataFrame to rename the data columns and create a plot. Since the signal has a different scale from the price and EMA data, define secondary underscore y to the signal column to plot it on secondary y axis on the right. The chart gives a clear indication of where to take long or short positions.

7. **Define the strategy with the signal**
Now we are ready to implement the signal in the strategy. In the previous lesson, we used algos SelectWhere to build the signal. Here the signal is not constructed directly from the price comparison, so we will use another way provided by bt. Call WeighTarget and pass the signal DataFrame. The signal value 1, minus 1 or 0 will dictate which period we will have long positions, short positions, or no positions.

8. **Backtest the signal based strategy**
Once we have the strategy defined, create and run a backtest and see how it performs.

9. **Plot backtest results**
Last, let's plot and review the backtest result. Overall the strategy is profitable based on the historical period backtested.

10. **Let's practice!**
Now it's time to practice!