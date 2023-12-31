1. **Portfolio composition and backtesting**
Working with individual stocks is relatively simple - but things get a lot more exciting once you begin building your first portfolio.

2. **Calculating portfolio returns**
You can think of portfolios as a bundle of individual stocks with different weights for each position. The return of a portfolio is a linear combination of the weights and returns of each position. This is assuming you're using discrete returns instead of log returns.

3. **Calculating portfolio returns in Python**
In Python, this entire operation can be performed in a single line if you have an array of portfolio weights and a DataFrame of stock returns. First, call the dot mul() method on StockReturns, pass in the portfolio weights, and set the axis to 1, for rows. This will multiply each portfolio weight by the corresponding returns column assuming they are in proper order. Then, call the dot sum() method, also with axis 1, to sum all the weighted returns in order to get the portfolio return. You'll be performing this operation a lot in this chapter. You can set the portfolio return equal to a new column in StockReturns if you wish to keep track of it easily.

4. **Equally weighted portfolios in Python**
Any good strategy should at least ideally outperform an equally weighted portfolio, which holds the same weight in every stock by default. To calculate an equally weighted portfolio, you first want to set numstocks equal to the number of stocks in your portfolio. Use np dot repeat() to set the portfolio weights, passing in 1 divided by the number of stocks as the first argument, and the number of stocks as the second argument. This creates an equally weighted array of weights with the proper length. You can then use the dot mul() and dot sum() methods as in the previous example. In this case, I use dot iloc to select the columns that contain stock returns.

5. **Plotting portfolio returns in Python**
Plotting daily stock returns in Python is easy. Assuming you have already computed returns by running the pct_change method on the data frame of adjusted prices, you can grab the column of returns and call plot. But this plot is noisy, right?

6. **Plotting portfolio cumulative returns**
Well that's because cumulative returns, or growth over time, is normally what you want to see. All you need to do is add 1 to the daily stock returns, take the cumulative product with the dot cumprod() method finally subtracting 1. In this example, I plotted two cumulative returns columns at once, using the dot plot method on the columns of interest.

7. **Market capitalization**
Market capitalization weighted portfolios are extremely common. The commonly quoted S&P 500 index, for example, is modeled after a market-cap weighted portfolio of the top 500 US stocks. While the S&P 500 isn't actually a real traded portfolio, it is a popular benchmarking strategy and many portfolio strategies and funds are based off of it.

8. **Market capitalization**
The market capitalization, or market cap, of a company is the total value of all outstanding publicly traded shares of the company at any given time.

9. **Market-cap weighted portfolios**
In order to calculate the market-cap weight of a given stock n, divide the market capitalization of that company by the sum of all the market capitalizations of all the stocks in your portfolio.

10. **Market-Cap weights in Python**
To do this in Python, first define a numpy array of the market caps of each company in your portfolio, then divide that array by the sum of the array. You can then use the market cap weights to calculate the market-cap weighted portfolio in the same way that you used the equal weights array to calculate the equally weighted portfolio.

11. **Let's practice!**
Now let's try some examples.