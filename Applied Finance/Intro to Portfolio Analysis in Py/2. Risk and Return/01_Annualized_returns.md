1. **Annualized returns**
Let's discuss different type of returns

2. **Comparing returns**
The different ways you can measure return can be confusing. First, there is such a thing as an annual return, which is simply the portfolio return over 1 year. Then, we have the annualized return. Now this is calculated by taking any time period, be it 4 months or 4,5 years, and calculate an annual rate of return that corresponds to the performance measured up to that point. You've already seen the average return in chapter 1, where we take the total return of a time period and spread it out evenly over the days, or months. Lastly, we have the cumulative or compounded return, which you also already know. It includes the compound effect of re-invested previous returns, like a compound interest.

3. **Why annualize returns?**
Let's have a look at this portfolio. Let's say you start with $100, and you double your investment in year 1. So by the start of year 2, you have $200, this gives you a return of 100%. Throughout the course of year 2, you lose $100 again, which is a percentage return of -50%. If you were to calculate an average return for the 2 year period, you take 100 minus 50, divided by 2 which equals a 25%. But in reality, you made nothing! So the average return is not a good measure of performance. Also, it's really difficult to compare performance if portfolios are of different lengths. How do you compare one that has traded for 6 months, versus one that has history for four years? Or even account for the compounding effect that takes place over the years? Well, you use the annualized return for that!

4. **Calculating annualized returns**
This is the formula you need to convert your return to an annual rate. The only thing you will need to change, is the period portion defined in 1/N. Suppose you would want to convert a 5 year total return to an annualized return. 1/N simply becomes 1/5. Now when you want to say convert a 6 month return to an annualized rate, you use 12/N which is now 12/6. And you could do it in the same way for days, using 365 instead of 1, and N in the days denomination. Remember to use the right mathematical order of operations here: Perform the operations inside the parentheses first, then apply the exponent, then perform the subtraction.

5. **Annualized returns in python**
Let's have a look at an example using the price of Apple. Let's say we want to calculate the annualized return from January 2015 till March 2018. First check the start date and the end of period over which you want to calculate the annualized return. You can use .head() and .tail() for this. In this case, the period covers 38 months, so let's assign that number to "months".

6. **Annualized returns in python**
Let's now calculate the total performance of the portfolio. Make sure to calculate total performance from the change in value over time, for example from prices, or the portfolio dollar value. Just be careful to use data on actual values here, not percentage returns.

7. **Annualized returns in python**
Now that we've got the total return rate and the number of months, we can fill in the formula for annualized returns. Since we are counting months, I use 12 over the number of months counted, in the exponential term. Also make sure to use brackets to execute this in the correct mathematical order. Suppose we want to count years instead of months, let's select 3 years. Then re-calculate the total return number for the three years, which I don't show here.

8. **Annualized return in Python**
Then, simply change the exponential term in the formula. Since we are counting years I change it to 1 over 3 years. And that's it, that's how to calculate your annualized returns.

9. **Let's practice!**
Let's calculate some annualized returns!