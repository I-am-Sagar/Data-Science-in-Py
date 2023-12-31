1. **VaR extensions**
In the previous exercises, we made a few dangerous assumptions about tail risk - but don't worry, we will address them now!

2. **VaR quantiles**
First, let's start with an easy one. There's no reason to be limited to VaR(95) or CVaR(95) - analysts often use the 99th quantile, or even the 99-point-9 quantile to get harsher forecasts of potential losses. If you always used the 95th percentile, you would tend to underestimate your risk in 5% of cases! To become more certain, you can raise the quantile. Of course, the higher the quantile, the higher the potential losses, and sometimes quite dramatically higher. This can lead to over-estimating risk, which can cause you to lose money by being too cautious. This is why testing different quantile parameters is important to striking the right balance between risk and reward.

3. **Empirical assumptions**
Now, up until this point, you have been estimating tail risk using historical empirical values, or in other words, using returns that have actually occurred. But there's an infinite amount of possibilities which have never occurred. For example, Apple stock may have fallen 3% in one day, but maybe it never fell exactly 3-point-125%, so this value would be missing from your simulation. A better way to go about things is to assume a probability distribution and to extract values from the quantiles of this distribution.

4. **Parametric VaR in Python**
Remember the normal distribution? Well, you can use the norm dot ppf function in Python to compute the parametric VaR of a normal distribution, in this case setting the mean and standard deviation equal to the mean and standard deviation of your historical returns. Of course, this doesn't address the non-normality of returns, but it's arguably more scientific than simply grabbing from a bucket of historical returns, and it allows for some flexibility when it comes to simulations later on in the chapter.

5. **Scaling risk**
All of your forecasts so far have also been for daily risk measures - but what about a 5 day forecast of risk, for example? 10 day? 21 day? Since losses and returns compound, you're going to need to scale these estimates using the square root of time.

6. **Scaling risk in Python**
For example, scaling a one-day VaR(95) estimate of -2-point-35 percent into a 5 day estimate dramatically increases the value to an estimate of -5-point-25 percent over 5 days. All you need to do is multiply the one-day var(95) by the square root of 5 to get the 5-day var forecast. If you wanted the 10-day var forecast, you would multiply by the square root of 10.

7. **Let's practice!**
Now let's try some examples.