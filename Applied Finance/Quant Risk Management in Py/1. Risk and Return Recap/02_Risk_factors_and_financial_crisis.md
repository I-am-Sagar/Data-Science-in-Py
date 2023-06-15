1. **Risk factors and the financial crisis**
In the previous lesson we reviewed how to quantify return and risk of a portfolio. Next we'll examine portfolio risk factors during the global financial crisis.

2. **Risk factors**
Quantifying risk involves volatility, a measure of the dispersion of portfolio returns around an expectation of what the returns will be, taking the sample average return as the expectation. But what variables or events will affect the expectation and the dispersion of returns? Such variables or events are known as the risk factors of a portfolio.

3. **Risk exposure**
A portfolio's risk exposure is the possible portfolio loss due to return volatility. Think of risk exposure as the potential negative impact of an uncertain future. For example, you may insure your home against flood, but have to pay an initial loss amount yourself. This is called a deductible. If the rest of a flood's damage is fully covered by insurance, your deductible is your risk exposure. Building a home in an area that floods frequently increases the volatility of flood damage, raising your deductible due to the increased risk exposure.

4. **Systematic risk**
We can classify risk exposure using risk factors. Some risk factors affect all portfolio assets in the same way. This is called systematic risk. If it is based upon a market aggregate, this is called market risk. Think of being on an airplane when one of the plane's engines fails. This failure affects everyone on the plane, and so is an example of a systematic risk. The price level of an economy is a systematic risk factor for a bond portfolio, because a higher inflation translates into a lower yield. The interest rate in an economy is also a systematic risk factor, because it changes the opportunity cost of investing in bonds and stocks. An economic boom or recession affects assets in a systematic way, driving broad market indices such as the S&P 500 or Dow Jones Industrial Average up or down.

5. **Idiosyncratic risk**
By contrast, idiosyncratic (or individual) risk factors are specific to a particular asset or asset class. Recalling our airplane analogy, not fastening one's seatbelt during severe turbulence is an example of a passenger's idiosyncratic risk. For a bond portfolio, the risk of default of the obligation issuer is an idiosyncratic risk. Characteristics specific to an asset's issuing firm, such as the size or book-to-market ratio, also contribute to idiosyncratic risk, as might shocks specific to an asset class or sector.

6. **Factor models**
Factor models assess the impact of systematic and/or idiosyncratic risk on returns. A factor model uses a statistical regression, often Ordinary Least Squares (or OLS), to regress returns (or returns volatility) on risk factors. Factor models such as the Fama-French model use a combination of market risk and idiosyncratic risk, where the latter is the size of the firm (market cap) and the firm's value (book-to-market ratio).

7. **Crisis risk factor: mortgage-backed securities**
The global financial crisis had no single cause. But we know ex-post that there was risk mismanagement within investment banks that were highly leveraged. This is because they used as loan collateral their holdings of mortgage-backed securities (or MBS). MBS are an asset class where each asset holds parts of many different mortgages. During the crisis these assets were mis-valued because the risk of default was highly correlated between homeowners. This severely underestimated how many people would have trouble paying back their mortgage at the same time. The high mortgage default destroyed collateral value. We can model MBS as a risk factor using the percentage of mortgages at least 90 days behind in repayment, the 90-day delinquency rate. The figure shows just how dramatically delinquency rates rose during the crisis.

8. **Crisis factor model**
Our factor model is then a regression of our investment bank portfolio returns against the delinquency rate of US mortgages. We can use the python statsmodels library to run the regression, creating an `OLS()' least squares object and fitting it to the data with the `fit()' method. The results are displayed using the `summary()' method.

9. **Regression .summary() results**
Although a regression summary returns a lot of information, for our purposes it is the statistical significance of the regression coefficient for mortgage delinquencies that concerns us most. In this example, the line in red indicates the coefficient value of 0-point-2256 and its t-statistic value of 2-point-275. The boxed number is the significance level--we generally want this to be 0-point-05 or less, to show that there is at least 95% confidence that the coefficient is statistically different from zero.

10. **Let's practice!**
In the following exercises you'll examine mortgage delinquencies as a risk factor for our investment portfolio. Good luck!