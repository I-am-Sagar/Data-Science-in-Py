1. **Trading signals**
Welcome back! In this chapter, let's learn how to build and backtest more sophisticated trading strategies.

2. **What are trading signals?**
First, let's discuss trading signals. Trading signals are triggers to long (buy) or short (sell) financial assets based on predetermined criteria. They can be constructed using one technical indicator, multiple technical indicators, or a combination of market data and indicators. Trading signals are commonly used in algorithmic trading, where trading strategies make decisions based on quantitative rules, and remove human discretion.

3. **A signal example**
Here is an example of a simple signal. It is constructed by comparing the price with its n-period simple moving average, or SMA. A long signal is triggered to buy the asset when its price rises above the SMA, and exit the long trade when its price drops below the SMA.

4. **How to implement signals in bt**
Previously, we discussed the 4-step process of defining and backtest trading strategies, and in particular, how bt uses individual algos as building blocks to handle trading logic. There are two main ways to implement signals in bt strategies. One way is to use algos SelectWhere to filter price levels for constructing the signal, which we will learn more about in this lesson. Another way is to use algos WeighTarget, which we will learn more about later.

5. **Construct the signal**
Let's build a signal based strategy with bt step by step using the price and SMA based signal previously mentioned as an example. First, we need to obtain the price data and calculate the moving average indicator. Here we use bt dot get to download the stock price data directly online. To calculate the SMA, we can apply dot rolling dot mean to the price data. Alternatively, we can use the talib library's SMA function.

6. **Define a signal-based strategy**
Now let's apply the signal to the strategy. This is handled by algos SelectWhere. It takes the argument price larger than SMA, which essentially is a Boolean DataFrame containing selection logic. If the condition is true, that is the price rises above the SMA, a long signal is triggered to enter long positions of the asset. There are a few simplifications to this strategy that are worth noting. First, we will use the strategy for trading one asset, or one stock at a time. When you are trading multiple stocks or assets, their price correlations are important to consider for proper position sizing and asset allocation. This is beyond the scope of this course. Another simplification we make is to assume there is no slippage or commission in the trade execution. Slippage is the difference between the expected price of a trade and the price at which the trade is executed, and often occurs when there is a supply and demand imbalance. Commissions are fees charged by brokers when executing a trade. These are practical considerations in real trading, but for now we will focus on the basics.

7. **Backtest the signal based strategy**
Once we have the strategy defined, let's create and run a backtest and to see how it performs.

8. **Plot the backtest result**
Last, let's plot and review the backtest result. The line chart shows how much the beginning capital balance increases over time from a baseline of 100. Note the flat line areas indicate periods when we don't have any positions, so the trading account balance does not change. Overall, the strategy is profitable based on the backtest performed on the historical data.

9. **Let's practice!**
Time to practice!

