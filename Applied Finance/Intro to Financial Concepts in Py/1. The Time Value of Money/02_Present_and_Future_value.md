1. **Present and future value**
Let's discuss one of the most fundamental financial concepts - Time Value of Money.

2. **The non-static value of money**
The value of money itself changes over time, and I can prove it with a few simple statements. Would you rather have 100 dollars in your pocket now, or 100 dollars in your pocket tomorrow? Of course, you'd rather have 100 dollars in your pocket today because it's more valuable to have it in your hand and to be able to do something useful with it today instead of tomorrow. Now, what if I offered you 10,000 dollars now, or 10,500 dollars one year from now? The decision becomes much harder to make. How much is the extra 500 dollars earned by waiting for a year really worth to you? The reason why it's difficult to make a decision is because you are actually comparing two different types of values, even though both offers are in dollars. The 10,000 is in present value dollars, and the 10,500 is in future dollars. You can't compare them directly.

3. **Time is money**
But you can, however, estimate the future dollar value of the 10,000 dollars in present value by figuring out what you could do with it over the course of a year. You could, of course, take the 10,000 dollars and stash it in a savings account at your bank, earning 1% per year, risk free. That's fine, but you can earn more if you take more risk. Take the 10,000 dollars, invest it in the stock market, and earn 8% per year on average. You could also lose money, or make more than 8%, but on average the return will be roughly 8%. Or finally, you could simply take the 10,500 dollars if you wait for one year.

4. **Comparing future values**
What you've done by examining these options is computed the future value of each scenario. This then allows you to compare the scenarios since they are all denominated in the same time-based currency, which we'll call future dollars in this example. Putting 10,000 present dollars in the bank will allow you to withdraw 10,100 future dollars one year from now. Option B is the best scenario, resulting in 10,800 future dollars on average after 1 year by investing 10,000 present dollars. However, there is of course a risk that your investment could be worth more or less than that value, but on average we can quantify the payout. This leaves you with a decision based only on risk. If you don't want any risk, take option C, which pays you 10,500 future dollars, guaranteed. If you aren't afraid of risk, take option B for an average return of 10,800 future dollars.

5. **Present value in Python**
Python has a module called numpy which will help us compute future and present values very efficiently. To compute the present value of $100 received 3 years from now at a 1.0% inflation rate, we can call NumPy's .pv() function, passing in the discount rate, number of periods, and the future value. Ignore the pmt parameter for now. This function returns a negative number when discounting from a future value to a present value, which simply means that you will have to spend cash, $97.05 to be exact, in these investment conditions in order to receive a future positive value of $100 after 3 years.

6. **Future value in Python**
If you want to compute the future value of an investment, on the other hand, we can use NumPy's dot fv() function, passing in the 5% average rate of return, the number of periods in the investment's lifespan, 3, and the initial investment value of 100 dollars, which should be negative, indicating that you are spending money now to get a future value later. As you would expect, the value return is actually positive, the reverse of the present value function, and once again we ignore the pmt parameter.

7. **Let's practice!**
Time to put this into practice.