1. **Mean, variance, and normal distribution**
Since financial risk can simply be thought of as a measure of uncertainty of future returns, it is good practice to examine the natural distribution of returns in order to better understand the risk of investments.

2. **Moments of distributions**
Probability distributions have common properties, known as moments, which can be analyzed and compared to other distributions. The first moment is the mean, or mu, which is essentially the average outcome of a random sample of the distribution. The second moment is the variance, which is simply the standard deviation, or sigma, squared. This is a measure of the variability in outcomes. The third and fourth moments are less commonly used. The third moment, skewness, is a measure of the "tilt" of a distribution, while the fourth moment, kurtosis, is an important measure of the thickness of the tails of a distribution. We'll get to those later.

3. **The Normal Distribution**
There are many different types of common distributions. You might be familiar with the Gaussian normal distribution if you've taken a statistics class before.

4. **The standard normal distribution**
The standard normal distribution is a special case of the normal distribution when sigma = 1 and mu = 0.

5. **Comparing against a normal distribution**
All normal distributions tend to have a skewness near 0 and a kurtosis near 3. Financial returns, on the other hand, tend to have positive skewness and a kurtosis higher than 3. This means financial returns tend to have a higher probability of both outliers and of positive returns than a normal distribution. We'll talk more about kurtosis and skewness later.

6. **Comparing against a normal distribution**
Here we compare the daily returns of IBM stock with a sample from the normal distribution with the same mean and standard deviation. There are statistical tests for normality(such as Shapiro-Wilk, Jarque-Bera, but a high kurtosis or large skewness is a simple indicator of non-normal returns.

7. **Calculating mean returns in python**
You can use Python to estimate the moments of a return distribution. To calculate the average daily return of an asset, or mu, assuming you have already calculated daily returns, simply use NumPy's mean function to compute the average. Now if you want to annualize that number, you'll first need to add 1 to the decimal before raising the quantity to the power of 252, which is the typical number of trading days in a year. For example, a daily return of just 0-point-03% works out to an annualized return of 7-point-85% when it is compounded every day for 252 trading days in a row.

8. **Standard deviation and variance**
The second moment of the distribution, the variance, which is the square of the standard deviation (or volatility), Volatility is one of the most important concepts for risk management in finance. Some traders simply refer to it as "vol" for short. The fundamental takeaway is simple: an investment with higher volatility is viewed as a higher risk investment. Volatility is just another measure of the dispersion of returns, just like variance.

9. **Standard deviation and variance in Python**
You can easily calculate the standard deviation of returns using the numpy std() function. If the returns are daily returns, then this function will output the daily standard deviation. In order to calculate the variance, simply square the standard deviation.

10. **Scaling volatility**
It's very important to understand that volatility scales with the square root of time. To properly scale the daily volatility of an asset, simply multiply the volatility by the square root of the number of trading days in a year.

11. **Scaling volatility in Python**
This is easy to accomplish using NumPy by simply multiplying the standard deviation of daily returns by the square root of 252.

12. **Let's practice!**
Time to put this into practice.