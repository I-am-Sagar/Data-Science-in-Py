1. **Budgeting project proposal**
In this chapter, you will combine everything you have learned so far to build a budgeting application to help you plan out your financial future.

2. **Project proposal**
You just got a new job as an entry-level Data Scientist at a technology company in New York City with a decent starting salary of 85,000 dollars per year. Unfortunately, after state and local taxes, you can expect to be sending roughly 30% back to the government each year. Living in such a high cost city is difficult, so you're going to have to create a very strict budget. Not to mention that conditions change over time. This is not a trivial project. You're going to have to forecast multiple economic variables. Rent and even the cost of food rises over time due to inflation, but luckily you're in a hot sector of the job market, and can expect decent salary growth over time.

3. **Constant cumulative growth forecast**
Before you get started, it might be useful to familiarize yourself with this pattern to be used for forecasting a variable with a constant growth rate, such as inflation. You can use NumPy's .repeat function to repeat a value any number of times in an array. If you use the growth rate as a decimal, such as in this example, you can add 1 to the array before taking the cumulative product. Subtracting 1 allows you to examine the cumulative growth in percentage terms. In this example, your investment has grown by 3% at the end of year 1, a total of 6.09% due to compounding by the end of year 2, and a total of 9.27% due to compounding by the end of year 3.

4. **Forecasting values from growth rates**
Now let's go one step further. You forecasted the growth rates, but what if you wanted to forecast the actual dollar value of the investment itself over time? All you would need to do is remove the - 1 which was subtracted in the previous example, and multiply the array by the initial value of your investment. In this example, your initial investment of 100 dollars is worth 103 dollars by the end of year 1, 106 dollars and 9 cents by the end of year 2, and 109 dollars and 27 cents by the end of year 3.

5. **Let's build it!**
Now it's time to put it all together and build a budgeting application.