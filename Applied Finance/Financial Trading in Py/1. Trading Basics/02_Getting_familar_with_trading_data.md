1. **Getting familiar with your trading data**
In this lesson, we will explore how to use Python to get more familiar with your trading data.

2. **Different types of traders**
We can categorize traders into a few types by how long they hold their trading positions, that is their holding periods. Day traders hold their positions throughout the day, but usually not overnight. They tend to trade frequently. Swing traders hold their positions from a few days to several weeks. And position traders hold their positions from a few months to several years.

3. **Resample the data**
Depending on the trading style, you may want to look at the time series data from different intervals, such as hourly, daily, weekly, etc. For example, a swing trader would prefer to have a daily price snapshot instead of one for every hour. You can use the "resample" method to sample a Python DataFrame. The code here demonstrates how to resample hourly data to daily or weekly data by specifying the parameter to be "D" and "W" in "resample" respectively. Typically we downsample from a narrower time frame to a wider time frame, such as from hourly to daily. This will result in a fewer number of rows, and the sampled data of the wider time frame is the aggregated result of the lower time frame. In this case, we use the mean, but it can also be the minimum, maximum, or the sum.

4. **Calculate daily returns**
It is also helpful to get familiar with your trading data by checking past returns and volatility. For example, we can use the "pct underscore change" method to calculate percentage change in the price, also known as price return. It computes the percentage change from the preceding row by default, so if we use daily price data, we will get daily returns. By plotting the results, we can obtain a quick understanding of typical return ranges and the volatility profile of a financial asset.

5. **Plot a histogram of daily returns**
It is also helpful to plot a histogram of daily price returns. A histogram is a visual representation of the distribution of the underlying data. To plot a histogram in Python, call the "hist" method on a DataFrame column. You can use "bins" to specify how granular you want the chart to be.

6. **Data transformation**
The financial market reflects fear, greed, and human behavioral biases, hence the market data is inherently noisy and messy. To make sense of the data, traders perform various data transformations and create so-called technical indicators. A very common indicator is the simple moving average or SMA. It is simply the arithmetic mean of the price over a specified period. The average is called "moving" because it is always calculated using the most recent n periods, and therefore moves along with the price on the chart. The SMA can be easily calculated using "dot rolling dot mean" on the price column, and specify the averaging period with the argument "window equals n".

7. **Plot the rolling average**
We can plot the SMA and the price in one chart. The plot includes a legend and shows that the moving average has a smoothing effect on the price. There is a rich library of technical indicators developed for trading. We will explore more details in chapter 2.

8. **Let's practice!**
Now let's do some practice!