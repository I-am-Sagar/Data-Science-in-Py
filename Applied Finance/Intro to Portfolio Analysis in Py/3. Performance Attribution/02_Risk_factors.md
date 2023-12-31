1. **Risk factors**
In this lesson, we're going to discuss factors.

2. **What is a factor?**
Factors are broad, persistent drivers of return. Just like food is made up out of nutrients like carbohydrates and protein, factors are the elements that make up a portfolio return. Stocks in your portfolio will exhibit certain characteristic, such as volatility, size, strong financial fundamentals, etc. Those characteristics will drive performance of these individual stocks, and in aggregate, form the factors in your portfolio. Factors are therefore measured by looking at the combined characteristics of the assets in your portfolio. Suppose you have many companies with a large size measured by market cap in your portfolio, that means that you have a large exposure to the size factor, or put differently, have a high correlation to the size factor. If those large sized companies do well in current financial markets, your portfolio will also perform well.

3. **Factors in portfolios**
We can broadly distinguish two types of factors, macro factors and style factors. Macro factors as those factors that affect financial markets broadly, volatility in interest rates, currency exchange rates, changes in governmental policies such as trade tariffs etc. Style factors are related to the characteristic of individual assets, such as price momentum, price volatility, accounting ratio such as book-to-price ratio etc.

4. **Using factor models to determine risk exposure**
Just like you would want to change the macro nutrients in your diet when you have a specific goal to reach (e.g. eat less carbohydrates to lose weight), you can similarly use factors as building blocks to create your optimal portfolio, and they are used in many ways. In the diagram on the left, factors are used tactically. For example one can invest in a single factor, say a low volatility one, because you believe the factor will outperform in the long run. By strategically managing and combining multiple factors in a portfolio, you can alter the risk return profile of a portfolio. Last, factors are also used in risk management, to check how well portfolios are diversified for example.

1 Source: https://invesco.eu/investment-campus/educational-papers/factor-investing

5. **Factor exposures**
The easiest way to check how your portfolio relates to investment factors, is to correlate your returns to the factor return. Those are publicly available. Let's have a look at some data. I've combined volatility factor returns, and the quality factor returns, with my portfolio returns in one DataFrame. The volatility factor typically combines stocks with a very low volatility, and the quality factor looks at high quality stocks, which are for example companies with a strong cash flow.

6. **Factor exposures**
Let's start with a quick correlation between our portfolio returns and the factor returns. Running df.corr gives me the pairwise correlation of the columns in the DataFrame. As a rule of thumb a correlation coefficient below -0.5 or above 0.5 means "there is a correlation". A coefficient close to zero means there is no correlation. You see that my portfolio returns are very highly correlated with the quality factor returns, suggesting that I have many stocks in my portfolio that would be considered high quality stocks. The correlation with volatility does not seem to significant.

7. **Correlations change over time**
Since your portfolios composition probably changes over time, as you change your portfolio weights regularly, so will your correlation to the factor returns change. It is therefore much more useful to look at a rolling correlation. In this example I take a 30 day window, and use the .rolling function available in pandas. I end with .corr(). This way, I can correlate my portfolio returns to the quality factor in a rolling window. Let's see what this looks like in a plot.

8. **Rolling correlation with quality**
Interestingly, you see that the correlation, although it remains relatively high, it does actually fluctuate and drop significantly in certain periods. The change in correlation over time is a result of both changes in our portfolio weights, but also due to changes in the quality factor. The quality factor returns change over time, as well as the underlying composition of companies that make up the factor.

9. **Let's practice!**
Let's practice!