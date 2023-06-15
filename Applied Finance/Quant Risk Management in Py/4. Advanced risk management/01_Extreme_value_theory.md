1. **Extreme value theory**
We've seen how to identify extreme events in data. Now we'll show how to manage the risk associated with these unlikely but potentially important events.

2. **Extreme values**
In the previous Chapter we saw that portfolio losses often suffer from extreme values, i.e. losses that are unusually large. These are also called losses 'in the tail' of the underlying distribution, since they occur relatively rarely. These 'tail losses' are very useful, because if modeled properly they contain precisely that risk of loss that we want to manage, i.e. losses exceeding some value.

3. **Extreme value theory**
Extreme value theory uses statistics to help understand the distribution of extreme values. In other words, it is a way to help model the tail of the loss distribution. One way to do this is called the "block maxima" approach. The idea is to take data over a time period,

4. **Extreme value theory**
break up that period into sub-periods,

5. **Extreme value theory**
called 'blocks',

6. **Extreme value theory**
and look at the maximum loss in each block. Another approach, called "peak Over threshold" or POT, makes all losses above a given level the dataset of interest. This is similar to what we did with extreme events in the previous chapter. For this chapter, we'll use the block maxima approach.

7. **Generalized Extreme Value Distribution**
Let's divide up the global financial crisis period 2007 - 2009 into weeks, and calculate the maximum loss of each week. This is easily done with a Pandas DataFrame or Series object using the `resample()' and `max()' methods. This is a new dataset of extreme values, here called ‘maxima’, and can be approximated with a new distribution. This distribution is the generalized extreme value distribution, or GEV. We can fit the GEV distribution to our 'maxima' data using the 'genextreme' distribution from 'scipy stats'. After importing the distribution, it can be fit as usual using the `fit()' method.

8. **VaR and CVaR from GEV distribution**
Using the GEV to compute VaR and CVaR estimates is done in exactly the same way as with a Normal distribution. For example, to find the 99% VaR, we use the percent point function `ppf()' and the fitted parameters we found earlier. Notice that this approach finds the maximum loss over a one week period at the given level of confidence. To FIND the 99% CVaR, recall that CVaR is the conditional expectation of the loss given the VaR estimate as the minimum loss. As you can see, ‘genextreme’ also has an `expect()' method, which is used to compute the CVaR in the same way as we've done in the past for the Normal distribution.

9. **Covering losses**
The VaR or CVaR estimate over extreme values is often used in the banking and insurance sectors to cover losses, which is an integral part of enterprise risk management. It is a regulatory requirement that banks keep enough reserves (sometimes called a reserve requirement) on hand to cover losses over a particular period (say, one week or 10 days) at a particular confidence level (say, 99%). We can use the VaR estimate from the GEV distribution to compute the required reserve, since it is a maximum loss, for a given period, at a given confidence level.

10. **Covering losses**
As an example, suppose that our investment bank portfolio is initially worth one million dollars. We'd like to know the reserve requirement at a 99% confidence level and a one week horizon. Using the VaR estimate we computed earlier, we have found the maximum loss that is estimated to occur 99% of the time over the course of one week. Multiplying the VaR estimate by our portfolio value will provide us with the estimated reserve requirement. If we suppose that the VaR estimate is 0-point-10, indicating a maximum loss of 10%, then the reserve requirement is one million multiplied by 10%, or $100,000. Notice that as the portfolio value changes, the reserve requirement will also need to change. How frequently the reserve requirement changes is given by legal regulation.

11. **Let's practice!**
You can test your knowledge of extreme value theory on both the investment bank portfolio and on the movements of a single asset, from General Electric, during the financial crisis. Good luck!

