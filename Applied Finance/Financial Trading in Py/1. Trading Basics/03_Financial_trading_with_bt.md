1. **Financial trading with bt**
In this lesson, we will learn about the bt package.

2. **The bt package**
Bt provides a flexible framework for defining and backtesting trading strategies in Python. A trading strategy is a method of buying and selling financial assets based on predefined rules. For technical trading, rules are usually based on technical indicators and signals. Backtesting is a way to assess the effectiveness of a strategy by testing it on historical data. The test result is evaluated to determine how it would have performed if used in the past, and whether it will be viable for further trading. To import the bt package, use import bt.

3. **The bt process**
There are four steps to define and backtest a strategy with bt. First we obtain historical price data of the assets we are going to trade. Second we define the strategy. Next we backtest the strategy with the historical data, and finally we evaluate the result.

4. **Get the data**
First, we need some price data. One way is to load data contained in a CSV file. With bt, we can also use its get function to fetch data online directly. By default, it downloads the "Adjusted Close" prices from Yahoo Finance by tickers. A ticker is an abbreviated identifier for a public-traded stock, and the "Adjusted Close" price is adjusted for events like corporate actions such as stock splits, dividends, etc. Prices of multiple securities can be downloaded at once by specifying multiple tickers within a single string separated by commas. Use "start" and "end" to specify the start date and end date.

5. **Define the strategy**
Next we define our strategy with bt dot Strategy. The "Strategy" contains trading logics by combining various "algos". This unique feature of bt allows us to easily create strategies by mixing and matching different algos, each of which acts like a small task force that performs a specific operation. Within "Strategy" we first assign a name. Then we define a list of algos in the square brackets. The first "algo" specifies when to execute trades. Here we specify a simple rule to execute trades every week using "RunWeekly". We will learn how to add more complex trading logic in later chapters. The second "algo" specifies what data the strategy will apply to, for simplicity we apply to all the data using "SelectAll". The third "algo" specifies, in the case of multiple assets, what weights apply to each asset. Here "WeighEqually" means, for example, if we have two stocks, we will always allocate equal amounts of capital to each stock. The last "algo" specifies that it will re-balance the asset weights according to what we have specified in the previous step. We now have a strategy that will execute trades weekly on a portfolio that holds several stocks. It will sell a stock that has risen in price and redistribute the profit to buy a stock that has fallen in price, maintaining an equal amount of holdings in each stock.

6. **Backtest**
Now we can perform backtesting. Use "bt dot Backtest" to combine the data and previously defined strategy, and create a "backtest". Call "bt dot run" to run the backtest and save the result.

7. **Evaluate the result**
We can use "dot plot" to plot and review the result. The line chart shows if we apply the strategy to trade Google, Amazon, Tesla stocks weekly, buy and sell them to maintain an equal weighted stock portfolio, in the six months during 2020 our portfolio will increase from 100 to 180. Not bad! We can also use "get underscore transactions" to print out the transaction details. We will explore more detailed performance statistics later in the course.

8. **Let's practice!**
Let's practice!

