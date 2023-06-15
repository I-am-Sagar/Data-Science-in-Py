1. **Measuring risk of a portfolio**
Let's talk about portfolio risk.

2. **Risk of a portfolio**
When you invest in stocks, you don't know beforehand what your return will be. Prices go up and down, so there is a degree of uncertainty, which implies that stock return is a random variable. The extend to which the actual returns are spread around their mean value is called variance. Here is the official formula for variance. It is a great indication of a stocks' riskiness or volatility. You might have come across variance in your statistics class.

3. **Variance**
Certain stock have a small variance, that means, their returns are always close the mean, like the returns distribution here in red. Sometimes, stocks have a high variance and are widely spread around the mean like the distribution here in blue. This might be easy to understand for a single asset, but how does this work for a portfolio? Well, portfolio variance isn't simply the sum of all variances of the underlying stocks. Due to correlation between the assets, it becomes more complicated.

4. **How do variance and correlation relate to portfolio risk?**
Since the assets in your portfolio correlate, i.e. move together or in the opposite directions, you intuitively understand this will influence the riskiness of your investment. That implies that correlation should be an ingredient in your portfolio variance. Also, the individual risk levels of the stocks are part of the calculation, as well as the portfolio weights. Lastly, you might come across "standard deviation" used as an indication of risk. This is simply the square root of the variance, and both are used in practice.

5. **Calculating portfolio variance**
Supposed I calculate the variance of a portfolio with 2 stocks. The portfolio variance is simply calculated by taking the weight times the variances sigma 1 and 2 for stock 1 and 2 respectively. I need to add a term to account for correlation between the stocks. That's why I multiply w1,w2, rho the correlation coefficient, and the variances sigma 1 and 2. This last term is actually what we call the covariance. So let's re-write the formula and insert the covariance, instead of the correlation times the variances.

6. **Re-writing the portfolio variance shorter**
Let's take that last equation from the previous slide. This one is long and difficult to work with. Hence, we can write it shorter and smarter if we use some matrix notation. It then becomes: weights transposed, times the covariance matrix, times the weights. The covariance matrix depicted here in the middle contains the variances on the diagonal, and the covariances between asset 1 and 2 on the off-diagonal terms. This is something we can actually implement easily in python.

7. **Portfolio variance in python**
Let's start from the beginning, by taking the price data again. First, remember to calculate the daily returns using the percentage change function, as we need to calculate variance from our set of returns, not from prices. Then, we can let python calculate our covariance matrix for us very easily. So now we almost have all ingredients to calculate the portfolio variance.

8. **Portfolio variance in python**
We need to take a short additional step, which is to annualize our volatility by multiplying it with 250, which is the amount of trading days in a year. Don't worry about it for now, you'll learn more about this in the next chapter. Last, we need the weights of our portfolio. We have five stocks here, so let's create a simple equal weighted portfolio.

9. **Portfolio variance in python**
Now apply the formula and multiply the transposed weights, with the covariance matrix and then with the normal weights again. Make sure to use the dot multiplier again. The numpy dot function takes only two arguments to multiply, so start with the covariance matrix with the normal weights, and then, multiply that whole thing with the weights transposed. And that gives you the portfolio variance. Last, let's take the square root of the variance to calculate the standard deviation, like this.

10. **Let's practice!**
Let's practice!