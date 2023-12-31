1. **Alpha and multi-factor models**
Now that we've covered the fundamental CAPM formula, we can start adding additional factors to enhance our analysis of portfolio returns.

2. **The Fama-French 3 factor Model**
The Fama-French 3 factor model is perhaps one of the most widely used models for portfolio management in finance, and was a real breakthrough for modern portfolio theory at the time. Developed by Eugene Fama and Kenneth French in the early 1990s, this model extends the CAPM model by adding the SMB, or size factor, as well as the HML, or value factor. The acronym for value, HML, stands for high minus low, whereas the acronym for size, SMB, stands for small minus big. This is because small stocks tend to outperform big stocks, so small stock returns minus big stock returns is essentially the small size premium. Value versus growth, or high minus low, on the other hand, is more cyclical. For example, during the crisis, value stocks outperformed, but during bull runs, growth stocks sometimes outperform.

3. **The Fama-French 3 factor model**
You can perform a Fama-French 3-factor analysis in Python by using the provided data, which includes the SMB and HML factor returns time-series, as well as the market excess returns as before with CAPM. The RF column is the risk free rate, and as you can see, it is essentially 0 during this time period.

4. **The Fama-French 3 factor model in Python**
Simply perform the same procedure as with CAPM, but add the SMB, size, and HML, growth, factors in the formula using the plus sign. The Fama-French model was a breakthrough because it vastly outperformed the CAPM model, explaining over 90% of portfolio variance on average compared to just 70% for CAPM. What's more, it simply made sense. Investors should be theoretically rewarded for being exposed to small cap stocks instead of large caps, as well as for being exposed to distressed or value stocks instead of the popular and premium growth stocks. More risk, more reward.

5. **P-values and statistical significance**
In a regression model, you will often need to extract the p-value of a coefficient, which you can do so using the dot pvalues() method on a fitted smf dot ols regression model in Python. Normally, p-values less than 0.05 are considered statistically significant. In this example, the HML factor, is statistically significant because the p-value is less than 0-point-05.

6. **Extracting coefficients**
Coefficients can be extracted from the fitted regression object using the dot params method. In this example, the portfolio has a positive exposure to the HML, or momentum factor, but a slight negative exposure to the SMB, or size. In other words, when small stocks rise, this portfolio tends to fall slightly. And when momentum stocks rise, this portfolio tends to rise significantly, at about 0-point-5 percent for every 1 percent rise in the growth factor.

7. **Alpha and the efficient market hypothesis**
Anything that couldn't be explained by the beta, size, or value factors in the model is called alpha, which is essentially an error term. Positive alpha is now popularly interpreted as outperformance due to skill, luck, or timing. Of course, for every fund with positive alpha, there is another fund with negative alpha since the weighted sum of all alpha in a market must be 0. This is because the weighted sum of the returns of all investors simply equals the market portfolio. Some economists believe in the efficient market hypothesis, which essentially states that the market prices all information. Therefore, any perceived "alpha" is simply the result of a missing factor in an a more complex economic pricing model. Of course, nobody seems to have figured out this model, but nearly every economist has certainly tried.

8. **Let's practice!**
Now it's time to build your own models!