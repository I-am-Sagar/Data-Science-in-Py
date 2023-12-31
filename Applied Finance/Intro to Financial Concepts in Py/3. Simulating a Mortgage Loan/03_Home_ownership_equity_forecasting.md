1. **Home ownership, equity and forecasting**
Even if you faithfully pay your mortgage over time and grow your ownership in your home, it still doesn't always mean it will be a good investment. Unfortunately, house prices fluctuate over time, and they don't always just rise. In fact, they can often fall quite sharply during times of crisis.

2. **Ownership**
At any given time, you can calculate the percentage of the home that you actually own, which is known as home equity, by dividing the cumulative principal payments you have made over time by the initial home value, adding the initial down payment percentage.

3. **Underwater mortgage**
When housing prices fall too fast, you can actually end up owing more on the mortgage loan than the house is worth itself. This is called an underwater mortgage. Unfortunately, this means that even selling the home won't be able to pay off the mortgage itself. The best case scenario is either refinancing (which is a restructuring of the loan) or continuing to pay the mortgage off in hopes that housing prices will rise. This is what happened to many people during the American Financial Crisis of 2007-2008.

4. **Cumulative operations in NumPy**
In the next set of exercises, you will use the cumulative numpy functions .cumsum and .cumprod. .Cumsum returns the cumulative sum of an array of numbers, instead of just a single number as a sum. For example, for the array 1, 2, 3, the .cumsum function actually returns an array of 1, 1+2, and 1+2+3, which is 1, 3, and 6. .Cumprod operates in the same way, except instead of a sum, it returns the product of all the numbers in the array. So the same array 1, 2, 3 now returns 1, 1*2, 1*2*3, which is 1, 2, 6.

5. **Forecasting cumulative growth**
You are now ready to calculate the cumulative growth forecasts. For example, to calculate the cumulative value at each point in time of a 100 dollar investment that grows by 3% in period 1, then 3% again in period 2, and then by 5% in period 3 - you can pass the array 0.03, 0.03, and 0.05, add 1 to the array, and then take the cumulative product of the array. The result is an array - 1.03, 1.06, 1.11 - which is the cumulative growth of the investment over each time period.

6. **Let's practice!**
Now it's your turn.