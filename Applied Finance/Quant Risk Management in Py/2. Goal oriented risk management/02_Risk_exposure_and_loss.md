1. **Risk exposure and loss**
Now that we've seen how to measure risk using VaR and CVaR, we can apply them to understand a portfolio's risk exposure. We'll also introduce another commonly used statistical distribution to help!

2. **A vacation analogy**
Let's say you’re planning a vacation, and you have to book your hotel reservations. The hotel gives you two payment options, one where you pay in advance at a lower rate, but without any chance of a refund; and one where you pay a higher rate after arrival, but you can cancel the reservation and pay 20% of the total amount as a fee.

3. **Deciding between options**
How you decide between payment options depends upon a few key factors. First, there is the chance that something will disrupt your vacation, such as illness, bad weather or other negative 'shocks', forcing you to cancel your trip. This is the probability of loss. Second, there is the amount you'll lose if there's a cancellation, which may be a fixed amount (such as an investment) or a conditional loss, such as VaR or CVaR. Third, you will have your own feeling for how much you would pay to avoid a negative shock. This is your risk tolerance.

4. **Risk exposure and VaR**
Risk exposure is the product of the probability of an event causing a loss, multiplied by the amount of a loss if one should occur. The amount of the loss is often the VaR, as it is the minimum amount 'in danger' of being lost at the VaR's confidence level. Suppose the chance of canceling your vacation due to illness is 10%. Let’s also say that the non-refundable hotel cost is €500. The 90% VaR is the amount in danger of being lost. Note that the 90% confidence level is derived from 100% minus the actual probability of loss in our example, which is 10%. Here, the 90% VaR is €500. The partially refundable hotel cost is €550. The VaR amount is the cancellation fee totaling €110.

5. **Calculating risk exposure**
Your risk exposure in the non-refundable case is 10% of €500, which is €50. In the partially-refundable case your risk exposure is 10% of €110, or €11. The difference is €50 minus €11, or €39. How do you choose between the two options? The final variable is the difference in hotel price, which is €550 minus €500, or €50. This is more than the difference in risk exposures, which is €39. So the hotel's two options are asking you about your risk tolerance: is it worth paying €50 more to avoid a greater risk exposure of €39?

6. **Risk tolerance and risk appetite**
You're likely risk-neutral if you prefer the non-refundable option over the partially refundable option. Since the €39 difference is less than the payment of €50 to avoid the greater risk exposure, risk neutrality implies you'll select the non-refundable option. You're likely risk-averse if you prefer the partially refundable option. You pay the €50 to avoid the risk of losing €39, because uncertainty is costly. This measurement of costliness expresses risk preference. Enterprise risk preference is usually called "risk appetite", while for individual investors it's often called "risk tolerance".

7. **Loss distribution - discrete**
As we've seen, risk exposure needs the probability of loss in order to be defined. In this simple example we assumed that risk was binary: you either did or did not go on vacation based upon an illness.

8. **Loss distribution - continuous**
In general, losses are assumed to take any value, leading to a continuous loss distribution. Until now we've focused on the Normal distribution because it is generally good for large samples, and is computationally easy to work with.

9. **Loss distribution - continuous**
For small samples, other distributions may be better, such as the Student's t-distribution. This distribution is widely used in portfolio analysis.

10. **Primer: Student's t-distribution**
Also called the capital "T" distribution, the Student's "t" distribution has fatter tails than the Normal distribution, which often occurs with portfolio returns and losses. As the sample size grows, the T distribution converges to the Normal distribution.

11. **T distribution in Python**
We can compute measures such as VaR and CVaR with the T distribution, just as we did with the Normal distribution. After importing the distribution from 'scipy stats', we fit the distribution to the data.

12. **T distribution in Python**
When the distribution is fit, the percent point function can be used to compute the VaR.

13. **Degrees of freedom**
One special characteristic of the T distribution is its degrees of freedom. The number of degrees of freedom is the number of independent observations. The degrees of freedom number affects the shape of the T distribution. It can be explicitly set with the `df' parameter, or estimated using the `fit()' method of the "scipy stats t" distribution.

14. **Let's practice!**
In the exercises to follow, you’ll work with the Student's t-distribution and derive risk exposure measures from it, adding another commonly used method to your toolbox.

