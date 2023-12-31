1. **What is financial trading**
Welcome! My name is Chelsea Yang and I work in quantitative finance. In this course, we will learn all about financial trading with Python.

2. **The concept of financial trading**
Financial trading is the buying and selling of financial assets, also called financial securities. People trade a variety of financial instruments, including equities: shares of stocks representing ownership of companies, bonds: debt instruments issued by the government or corporations, forex or foreign exchange market of currencies, commodities such as gold, silver, and oil, and cryptocurrencies like Bitcoin.

3. **Why people trade**
People trade to make a profit by taking calculated risks. A trader makes a profit when buying a security at a lower price and selling later at a higher price, known as going long. Conversely, they may sell a (borrowed) security at a higher price and buy it back at a lower price, known as going short. Institutional traders, such as hedge funds or investment banks, may trade in order to hedge financial risks, provide market liquidity, or re-balance their portfolios. Retail traders are mostly trading for their own accounts, sometimes as a side hustle.

4. **Trading vs. investing**
The main difference between trading and investing is time-horizon. Trading typically has a shorter holding period, ranging from days to months. Investing has a longer time horizon, ranging up to years or even decades. Trading focuses on short-term market trends and tries to profit from volatility and price fluctuations. Investing focuses on market fundamentals, macroeconomic environment, and aims to ride on big trends that can span years. Finally, whereas investors typically take long positions, traders take both long and short positions in order to profit from both upward and downward price movement. In this course, we will focus on technical analysis based financial trading. Generally, a technical trader analyzes historical patterns of trading data, and implements trading strategies based on indicators, signals, and rules in order to profit from possible future price movement.

5. **Financial time series data**
For financial trading, you will mostly work with time series data of security prices. Time series data is a sequence of data points indexed in time order. Here we have some Bitcoin historical price data saved in a CSV file. We load it as a DataFrame with the "read underscore csv" function from pandas, which has been imported as pd. We use "index underscore col" to specify the "Date" column as the index, and set "parse underscore dates" to True to parse the index in DateTime format. The "head" method displays the top 5 rows of the data. Daily data typically includes open, close, and daily high and low prices, as well as volume.

6. **Plot line chart of time series data**
We can plot the time series data with the "plot" function, using the "matplotlib show" function to display the plot. The resulting line chart gives us information on past price patterns.

7. **Candlestick chart**
We can also visualize the price movement using a candlestick chart. Each candlestick shows price information for one-period, for example one-day. Within each candle we can see: open and close in the candle body and high and low in the candlewick. Typically a white or green candle represents the close price above the open price, and a black or red candle represents the close price below the open price.

8. **Plot candlestick chart with Python**
We can easily plot candlestick charts with the Python package "plotly dot graph underscore objects". We import the package as go and then define a candlestick using the time series data index, ie Date, and the "Open", "High", "Low", "Close" columns in the price data. We then call Figure to create a plot, passing in our data as a list. Finally, we call the "show" method to display it. This will create an interactive chart.

9. **Let's practice!**
Let's practice!