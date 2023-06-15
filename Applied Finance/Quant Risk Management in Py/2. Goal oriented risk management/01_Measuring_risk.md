1. **Measuring Risk**
We've examined how the efficient frontier allows us to trade off risk and return. But how do we measure risk? Here we'll estimate how much a portfolio stands to lose, using the Value at Risk and Conditional Value at Risk statistics.

2. **The Loss Distribution**
Suppose a European investor holds a foreign exchange portfolio holding 100 US Dollars. The investor's portfolio exposes them to the Euro for Dollar exchange rate, since the investor ultimately values the portfolio return in Euros. If the starting value of the portfolio is 100 Euros, the exchange rate is 1 Euro per Dollar. But in general, the portfolio's value will fluctuate, because the exchange rate 'r' is random. The loss will be the difference between the original portfolio value of 100 Euros and the new value of 'r' times 100. A loss distribution tells us a portfolio’s future potential losses due to the random nature of its risk factors, when holdings are fixed over a time horizon.

3. **Maximum loss**
For financial institutions, an upper bound on losses is crucial. Because risk factors are random, it is usually not possible to bound losses with 100% certainty. Instead, we look for the likelihood that losses will remain capped by an upper bound. This likelihood is called the confidence level. The confidence level allows us to express questions about the maximum loss from a likelihood perspective, such as 'What is the maximum loss that would take place 95% of the time?'. In this question, the confidence level is 95%.

4. **Value at Risk (VaR)**
The Value at Risk statistic, or “VaR”, measures the maximum portfolio loss for a given confidence level. VaR is usually expressed for 95%, 99% or 99-point-5% confidence levels. In our portfolio example, if the Euro to Dollar exchange rate remains above 40 Euro cents to the dollar 95% of the time, then the minimum portfolio value is 40 Euros and so the maximum loss is 60 Euros. Thus the 95% VaR is 60 Euros.

5. **Conditional Value at Risk (CVaR)**
The conditional Value at Risk statistic, or CVaR, asks what the expected loss will be provided that the loss is greater than the VaR. CVaR is the expected value of the loss over the tail of the loss distribution. Note that CVaR is sometimes expressed using the confidence level, 95%, and sometimes with the significance level, which is 100% - the confidence level, or in this case 5%. We'll use the first convention in this course. In the figure, we see the loss distribution in red, the 95% VaR as a blue line (here equal to about 1-point-64), and the tail of the distribution exceeding the VaR as a shaded blue area. The expected value of the tail is the CVaR, which is the expected loss in the worst 5% of outcomes. Computing the CVaR requires the loss distribution, the maximum possible loss (which may be infinite), and the minimum possible loss (which is the VaR). In our foreign exchange example, the 95% CVaR would be the expected loss when the portfolio has already lost 60 Euros, in other words when the portfolio value is smaller than 40 Euros.

6. **Deriving the VaR**
To derive the VaR, first specify the confidence level. Then create a Pandas Series object from the observations, taken here to be portfolio losses (this can also be derived from a probability distribution). Next, calculate the quantile of the loss distribution corresponding to the confidence level. We can use the `quantile()' method attached to the Series object. The computed quantile is the VaR at that confidence level. If we know losses are distributed according to a statistical distribution like the Normal distribution, we can also use the `ppf()', or percent point function, to find the VaR, as we'll do shortly.

7. **Deriving the CVaR**
To derive the CVaR, first specify the confidence level. Then specify the loss distribution sample. Here, instead of a general set of observations, we'll use as our example portfolio losses a random sample from a Normal distribution using the 'norm' object from 'scipy stats'. Next we calculate the VaR at this confidence level, using the 'norm' object's `ppf()' method. We could also have used the quantile method on 'losses', if we wished, but the percent point function is very useful when the distribution is known. The VaR is used as the lower bound to find the expected value of the tail loss. If losses are Normally distributed, the `expect()' method attached to the 'norm' object will compute the CVaR. If losses are not Normally distributed, the expected value is computed using the integral shown previously, in the definition of the CVaR.

8. **Visualizing the VaR**
We visualize the VaR by plotting the loss distribution and showing where the quantile value is located, with a vertical line. Here we plot a histogram of 1000 draws from a Normal distribution, to represent the loss distribution.

9. **Visualizing the VaR**
A vertical line is drawn at the quantile values for 95%,

10. **Visualizing the VaR**
99%

11. Visualizing the VaR
and 99-and-a-1/2%. Notice how the vertical line moves further and further to the right, showing how the VaR increases as the confidence level grows.

12. Let's practice!
Now it’s your turn! Test your knowledge of VaR and CVaR by creating and plotting a loss distribution, computing statistics, and adding them to your loss distribution plot.