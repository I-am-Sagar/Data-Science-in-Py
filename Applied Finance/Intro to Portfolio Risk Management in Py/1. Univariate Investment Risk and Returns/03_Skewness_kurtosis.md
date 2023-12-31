1. **Skewness and kurtosis**
Daily volatility and mean give you a good indication of daily risk and return, but skewness, kurtosis, and scaled volatility will help you build a more holistic view of risk.

2. **Skewness**
The third moment, skewness, can be thought of as a measure of how much a distribution leans to the left or right. Negative skew is a right-leaning curve, while positive skew is a left leaning curve. In finance, you would tend to want positive skewness, with a higher probability of significantly good returns on the right hand side of the distribution, and a compressed, predictable left-hand distribution of negative returns.

3. **Skewness in Python**
To calculate the skewness of a return distribution, simply call the skew() function after importing skew from scipy dot stats. Be sure to drop any NA values using the dropna() method. Skewness above 0 indicates possible non-normality, which once again you can expect to find in financial returns.

4. **Kurtosis**
Kurtosis is a measure of the thickness of the tails of a distribution, which can be used a proxy for the probability of outliers. If you recall, normal distributions tend to have a kurtosis near 3. Most financial returns are leptokurtic, which simply means that they tend to have positive excess kurtosis, or kurtosis greater than 3. Since kurtosis is so often compared to a normal distribution, many functions in Python will automatically return excess kurtosis, which is essentially the sample kurtosis minus 3, which helps demonstrate whether the probability of outliers is higher or lower than a normal distribution. If excess kurtosis is higher than 0, the kurtosis is higher than a normal distribution.

5. **Excess kurtosis in Python**
In SciPy, for example, the kurtosis function is actually computing excess kurtosis. If you wanted to calculate the true sample kurtosis, you would actually need to add 3 to the result. But for most cases, you're going to be interested in excess kurtosis anyways, so this functionality is fine as long as you are aware of it. In finance, high excess kurtosis is an indication of high risk. When large movements in returns happen often, this can be a very bad thing for your portfolio if it moves in the wrong direction. High kurtosis distributions are said to have "thick tails", which means that outliers, such as extreme negative and positive returns, are more common.

6. **Testing for normality in Python**
Before we move on, let me briefly add one final tool to your arsenal. If the kurtosis of a distribution is greater than 3, and the skewness is non-zero, the data is most likely non-normal. But what if the values are close to, but not quite normal? You can use the Shapiro-Wilk statistical test to estimate the probability that the data is normally distributed. The null hypothesis of the Shapiro-Wilk test is that the data are normally distributed, and when the p-value returned is less than or equal to 0-point-05, that means you can safely reject the null hypothesis and assume that the data are non-normal.

7. **Let's practice!**
Now it's your turn.