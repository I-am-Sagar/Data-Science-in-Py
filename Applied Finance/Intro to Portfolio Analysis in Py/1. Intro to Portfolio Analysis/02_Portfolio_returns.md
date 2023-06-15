1. **Portfolio returns**
Let's discuss portfolio weights and returns.

2. **What are portfolio weights?**
The portfolio weight of an asset in your portfolio, is the percentage of the total value invested in that particular asset. The portfolio weights summed together add up to 100%. By setting many relatively small weights, you can diversify your portfolio. The larger the weights to individual stocks, the more exposed you are to fluctuations of that particular stock.

3. **Calculating portfolio weights**
The easiest way to calculate a portfolio weight, is to divide the dollar value of a security by the total dollar value of the portfolio, which gives you the percentage. Portfolio weights are key in expressing your investment strategy. I already mentioned the equal weighted and market cap weighted portfolios, which are created by setting the weights a certain way. The portfolio manager's job is to determine the optimal portfolio weights, given certain risk and return constraints, and change those as market conditions change.

4. **Portfolio returns**
Portfolio returns are changes in value over time. In this example, you see how a portfolio's value in red changes over the time span of a year. You can also compare it to the line in blue, which is the S&P500 return over that year. Returns are an indication of how well a portfolio performed over time.

5. **Portfolio returns**
Returns can be calculated, as stated by this equation by taking the difference in value over a time period, say from time t-1 to t. Divide the change in value over the initial value at t-1, which gives you the return as a percentage change. The historic returns are also used to calculate a portfolio's expected return for the future. Always take into consideration the probability that an asset will achieve its historical return given the current investing environment. Some assets, like bonds, are more likely to match their historical returns, while others, like stocks, may vary more widely from year to year. There are different types of returns, which are a common cause of confusion. Most common are average returns, which are often the geometric mean of a return series over a given time span. This is not the same as cumulative return, which is the total return over a period, active return, which is the relative performance to a benchmark, or annualized returns, which are covered in the next chapter.

6. **Calculating returns from pricing data**
Let's calculate portfolio returns. Let's take price data from these three stocks, Apple, Amazon and Tesla. The portfolio return will be today's value minus yesterday's value, divided by yesterday's value. You can simply use the percentage change function to do this for you. The newly created daily returns DataFrame tells you by how much percent the price of a stock has changed, relative to yesterday's value.

7. **Calculating returns from pricing data**
Now let's assign some portfolio weights to our three stocks. And let's take the mean of the daily returns value. This is very straightforward because we now know what the average daily return was for each stock in our data. By then multiplying the average returns, with their associated weight, to get the average daily return for the portfolio.

8. **Calculating cumulative returns**
The cumulative return allows you to track total performance over time. First create a daily returns series for the portfolio. You do so by multiplying the weights with the returns. You need to use to dot multiplication, as you're multiplying a series of weights with a dataframe of returns, and do so element-wise.

9. **Calculating cumulative returns**
Now it's time to go from daily returns, to cumulative returns. Just like with interest in your bank account, returns compound over time. That means you are multiplying percentage change over percentage change. You need to therefore use the cumulative product function like this. (1 + daily return) is your multiplication factor over time, just like with compounding interest. Now let's plot it.

10. **Cumulative return plot**
And here you have it, your daily cumulative returns of your portfolio containing Apple, Amazon and Tesla.

11. **Let's practice!**
Let's practice!

