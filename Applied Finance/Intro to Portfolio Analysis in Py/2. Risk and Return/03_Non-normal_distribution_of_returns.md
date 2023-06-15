1. **Non-normal distribution of returns**
Let's dive deeper into return distributions.

2. **In a perfect world returns are distributed normally**
Let's have a look at the distribution of monthly returns from the S&P500. In a perfect world we assume all distributions roughly look like this, like a normal distribution. In most of the calculations we do in portfolio analysis, we assume all returns are distributed this way. But what if they are not?

1 Source: Distribution of monthly returns from the S&P500 from evestment.com

3. **But using mean and standard deviations can be deceiving**
We calculate the mean and the standard deviations and use those as an indication of expected return, and volatility. But hold on for a second, and look at these two distributions. They actually have the same mean and standard deviation! As you can imagine, your experience investing in a portfolio with one or the other distribution is going to be very different.

1 Source: “An Introduction to Omega, Con Keating and William Shadwick, The Finance Development Center, 2002

4. **Skewness: leaning towards the negative**
That's why you need to look further than the mean and standard deviation, and look at skewness and kurtosis. You might have come across these things in your statistics class. First of all, skewness tells you whether the distribution is symmetrical, or whether it has a "bump" towards the left or the right from the middle.

5. **Pearson’s Coefficient of Skewness**
Pearson's coefficient of skewness is calculated by looking at the difference between the mean and the median, which you saw in the picture earlier. You can use it to assess how badly asymmetrical your distribution is. You can also use the following rule of thumb for that. If it's above 1 or less than -1, it's highly skewed. Moderate skewness happens when the coefficient is between 0.5 and 1 or -1 and -0.5, and between -0.5 and 0.5 there is no skewness. If the skewness coefficient is positive, it means that the distribution has a bump towards the left of the middle. That's not good for investing as a large proportion of returns are going to be below the mean.

1 Source: https://brownmath.com/stat/shape.htm

6. **Kurtosis: Fat tailed distribution**
Alternatively kurtosis tells you how much of the observations are centered in the middle, or alternatively how much observations are in the tail of the distribution. You can imagine that a fat-tailed distribution like the one pictured here, can mean that your portfolio returns are quite often in the extreme ends of the distribution, which is often not a good thing.

1 Source: Pimco

7. **Interpreting kurtosis**
High kurtosis means that a lot of the variation is coming from extreme events, that basically corresponds to the fat tails we saw earlier. Important to know is that a normal distribution has kurtosis of 3. A kurtosis of less than 3 means returns are more concentrated around the mean, and less in the tails. Anything above 3 implies you have slightly fatter tails, which is undesirable for investors.

1 Source: https://brownmath.com/stat/shape.htm

8. **Calculating skewness and kurtosis**
Skewness and kurtosis need to be calculated from a return series. Let's have a look at the Apple prices we used earlier. First, you need to make sure the prices are converted into returns, remember to use the percentage change function for that. Now that we have the returns, let's plot them in a histogram, visualizing your returns is always a good idea and will give the first clues about whether they are normally distributed or not.

9. **Apple returns**
This is what the Apple returns look like over the period from 2015 to the end of 2018.

10. **Calculating skewness and kurtosis**
And skewness and kurtosis can easily be obtained using the following pandas commands, you can run these on any series or pandas DataFrame. As you can see the mean return is very close to zero. The distribution is symmetric as the skewness is between -0.5 and +0.5, which is a good sign. However, kurtosis is bigger than 3 which means it's very slightly fat tailed.

11. **Let's practice!**