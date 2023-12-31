1. **The Capital Asset Pricing Model**
Factor analysis is the practice of using known factors such as the returns of large stocks or growth stocks as independent variables in your analysis of portfolio returns, and there are many different factor models in use today.

2. **The founding father of asset pricing models**
In this chapter, we'll start with the first and most popular model - the Capital Asset Pricing Model, otherwise known as CAPM.

3. **Excess returns**
But before we dig into CAPM, let's first talk about excess returns. Assume you live in Brazil, and the return on deposits at your bank is 15% per year. If you earned 10% by investing in the stock market that year, your excess return was actually negative 5%. If that same portfolio was a US portfolio, where the risk free rate of return was only 3% per year, your excess return would have been 7%. Since the recession in 2008, the US has had a risk free rate close to 0, but it has been rising steadily, albeit slowly, since.

4. **The Capital Asset Pricing Model**
The Capital Asset Pricing Model, or CAPM, is the cornerstone of many different financial formulas. CAPM relies on a single important factor, Beta. Beta is your exposure to a regional broad market benchmark portfolio. The risk free rate used is also regional, and is subtracted from both your portfolio and benchmark portfolio returns to allow for a better analysis of your true exposure. A high beta means a high market exposure, and a low or even negative beta means low or negative exposure to market movements.

5. **Calculating Beta using co-variance**
Beta can be calculated by dividing the covariance between your portfolio and the benchmark by the variance of the benchmark. However, this approach doesn't allow for additional factors to be easily incorporated into the analysis.

6. **Calculating Beta using co-variance in Python**
To calculate beta in Python, first find the co-variance between your portfolio and the benchmark index using the dot cov() method. Now calculate the variance of the excess market returns using the dot var() method. Finally, to calculate the portfolio beta, divide the co-variance coefficient by the benchmark variance.

7. **Linear regressions**
Regressions are a common way to analyze the impact of independent variables, or factors, on a dependent variable. In this case, you are regressing your portfolio excess returns against the market excess returns, which is one of your factors. Beta is simply the coefficient of this regression.

8. **Calculating Beta using linear regression**
The regression analysis is easy to perform in Python, but it will require a few extra steps. First, you'll need to import statsmodels dot formula dot api as smf. Next, use the ols() function, and pass in the column names of your independent and dependent variables, separated by the tilda. After the formula is defined, you then need to call the dot fit() method on the object. This will perform the regression. You can analyze your regression results using the dot summary() method, but in this case all we really want is the beta, which can be extracted by calling the dot params(), and indexing for the Market_Excess coefficient, which is the beta.

9. **R-Squared vs Adjusted R-Squared**
The r-squared value of a regression is a measure of the percent of variance of the regressed variable explained by the regressor factors, ranging from 0 to 100%. While it may sound nice to have a model that explains nearly 100% of the variance, you have to watch out for over-fitting. One way to avoid this is to penalize the regression for the number of added variables, which is exactly what the adjusted r-squared does. For this reason, you will compare the adjusted r-squared values of multiple models in this chapter.

10. **Let's practice!**
Time to calculate your first pricing model!