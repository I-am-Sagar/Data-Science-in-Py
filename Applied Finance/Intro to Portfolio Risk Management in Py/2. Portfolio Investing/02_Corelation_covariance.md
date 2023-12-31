1. **Correlation and co-variance**
Modern portfolio theory teaches that you can actually build a portfolio of assets which has less risk than any of the underlying assets alone. How is this possible? In short - it's all about correlation and co-variance.

2. **Pearson correlation**
Pearson correlation is a measure of the linear correlation between two variables, in our case, between the returns of two stocks. Pearson correlation ranges from -1 to 1 where 1 is perfect positive correlation, -1 would be perfect negative correlation, and 0 would be no correlation.

3. **Pearson correlation**
You can calculate the correlation coefficient for every pair of stocks in your portfolio, and this results in a matrix of correlations. I won't bore you with the formula, since you're simply going to be using Python to easily calculate the pearson correlation matrix.

4. **Correlation matrix in Python**
Assuming you have a pandas DataFrame of stock returns, all you need to do is call the dot corr() method on the DataFrame. You'll notice that the diagonals of the matrix are always equal to 1. This is because any variable or asset will always be perfectly correlated with itself, of course.

5. **Portfolio standard deviation**
Now we can use the correlation in a formula to calculate the portfolio standard deviation for a two asset portfolio. But if you have more assets in your portfolio, this formula will get very complicated very quickly. This is where the covariance matrix will come in handy.

6. **The Co-variance matrix**
Correlation is actually a normalized measure of the co-variance. Co-variance measures the joint variability of two random variables, and in finance, the co-variance matrix is often used for portfolio optimization and risk management purposes. There are many different ways to derive a co-variance matrix, but of course for this course we'll just use a handy Python function!

7. **The Co-variance matrix in Python**
All you need to do is call the dot cov() method on the DataFrame of daily stock returns.

8. **Annualizing the covariance matrix**
Now, you might recall that the variance of a stock scales linearly with time, or the volatility with the square root of time. In this case, since it is a variance-covariance matrix, all you need to do to annualize the covariance matrix is multiply it by the number of trading days in a year, that is 252.

9. **Portfolio standard deviation using covariance**
Remember that nasty formula for portfolio standard deviation using correlation? Well, we can collapse the formula into a much simpler one using the covariance matrix, but there's a few new concepts to introduce as well.

10. **Matrix transpose**
The first is the transpose operation, represented as the capital T. This simply means you flip the dimensions of a matrix, as if you are rotating it by 90 degrees.

11. **Dot product**
The second is the dot product operator. Also known as the inner product, it is quite common in linear algebra. Don't let it scare you, it's simply a shorthand for the sum of the products of the elements of both matrices.

12. **Portfolio standard deviation using Python**
Don't worry, this is easy to do in Python as long as you keep track of everything. Assuming you have already calculated portfolio weights and the covariance matrix, follow the formula from the previous slide to calculate portfolio standard deviation. If you pass in the daily covariance matrix, the result is daily portfolio volatility. Likewise if you pass in an annualized matrix, the portfolio volatility will be annualized as well. The dot T operator in numpy does the transpose of the weights array, and the np dot dot() and np dot sqrt() functions allow you to compute the dot product and square root, respectively.

13. **Let's practice!**
Now let's try some examples.

