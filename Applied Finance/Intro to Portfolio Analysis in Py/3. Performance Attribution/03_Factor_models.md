1. **Factor models**
In this video, you'll learn about the Fama French Multi factor model.

2. **Using factors to explain performance**
In the previous video you learned that factors help you manage your portfolio risk, and also help explain performance of your portfolio. There are commonly used factor models, that provide a framework for relating factors to portfolio returns. Those models have been widely tested and are also widely used. One of the most famous factor models, is the Fama French 3-factor model.

3. **Fama French Multi Factor model**
This is what the Fama French model looks like, it explains your portfolio returns using these three factors: MKT is market return minus the risk free rate. SMB stands for Small Minus Big: this measures the excess return of stocks with small market cap over those with larger market cap. - HML stands for High Minus Low. It's a value factor, and measures the excess return of value stocks, where value stocks typically have a higher book to price ratio (B/P) compared to other stocks. The betas tell us how that specific factor can explain the movement in our portfolio returns.

4. **Regression model refresher**
You might have noticed that the Fama French model looks very much like a linear regression. Here's a quick refresher; a linear regression is a model that tries to fit a straight line to your data points. It does so by trying to minimize the overall error, aka the distance between the blue dots and the red line. The betas in the Fama French model are the same as the beta coefficients in a linear regression: they are the slope of the line, and tell you how much your portfolio return changes if the factor changes by 1 unit.

5. **Difference between beta and correlation**
You might wonder, how are the betas different, from correlations, so let's highlight some important differences here. When the factor return changes by 5%, beta tells you how much your portfolio return will change. Correlation is not that specific. It tells you in general, how much of the variation in returns is explained by the factor movements. The correlation is a standardized measure between -1 and 1, and beta is not and its size has meaning. Also, the correlation has no direction, it tells you how two things are related. Beta only applies to the effect of X on Y, not visa versa.

6. **Regression model in Python**
Let's now run a quick linear regression model in Python. You can do this with statsmodels, or scikit-learn, but let's take the first option, as it has a nice summary function. First, let's import statsmodels. You can define the linear regression model by running sm.OLS, which stands for "Ordinary Least Squares" and fit it to your data with the function "fit". Here I use the the momentum and value factor returns as explanatory variables for the S&P500 returns. You can then easily obtain predictions with the model.predict function, or extract the betas using the parameters function.

7. **The regression summary output**
Model summary gives you an extensive output of your linear model. The most interesting part is the section at the bottom. Coef tells you what the beta coefficients for each factor are. The t-statistic and P-value indicate whether the beta coefficient is significant i.e. whether it has actual explanatory power in explaining the returns of the S&P500. Without going into much detail now, a p-value below 0.05 typically implies the coefficient is significant.

8. **Obtaining betas quickly**
Suppose you are only interested in the betas of your investment factors. You can get these much quicker by running the following functions in one straight line of code. And let's print the outcome nicely like this. Now let's use the linear regression model to create a Fama French factor model in the exercises.

9. **Let's practice!**
Let's practice!