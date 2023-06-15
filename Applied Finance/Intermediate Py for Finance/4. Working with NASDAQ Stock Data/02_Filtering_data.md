1. **Filtering data**
Now that you know how to peek and understand your data, it's time to learn how to filter it.

2. **Introducing the data**
For this lesson we'll be using a DataFrame, named prices, which contains the highest prices for various stocks over a six month period.

3. **Introducing the data**
The DataFrame has columns for the date, stock transaction, and the highest price of that stock for that day.

4. **Introducing the data**
We can use describe

5. **Introducing the data**
to see that the prices range from a minimum of $227.49 to a maximum of $2185.95.

6. **Introducing the data**
And use describe on objects to see that there are three distinct values in the symbol column. But what if you want to select all of the rows for a particular stock, or all of the rows whose price is above a certain value? In this lesson, we will learn how to do both.

7. **Comparison operators**
You have already been introduced to the comparison operators for less than, less than or equal, greater than, greater than or equal, equal, and not equal.

8. **Column comparison**
You can use these operators to compare a value to those in a column.

9. **Column comparison**
The result will be a sequence of Boolean values, True for each row whose value is true for the comparison, and False for the rest. Here True is returned for every row where the value in the column High is greater than $2,160, and False for the rest.

10. **Column comparison**
Here we use the equals operator to compare the values in the column Symbol with the symbol for Apple computer.

11. **Column comparison**
True is returned for every row that represents Apple stock.

12. **Masking by symbol**
Remember that when we pass a sequence of Boolean values to a DataFrame's .loc[] operator, a new DataFrame is returned containing only the rows matching the True. If we take the results of our comparison on the Symbol column, and use it as a argument to .loc[], the resulting DataFrame will only have the rows which are for Apple.

13. **Masking by symbol**
We can use .describe() on the Symbol column, and see that the new DataFrame has 126 rows, only one unique value for the Symbol, and that this value is 'AAPL'.

14. **Masking by price**
We can do the same thing with the comparison we made on the High column. Assign the result of the comparison to a variable and then use the variable with the DataFrames .loc[] operator.

15. **Masking by price**
When we call .describe() on the resulting DataFrame, we see that six rows are returned and the minimum value is higher than our conditional value.

16. **Pandas Boolean operators**
Pandas offers operators to combine the results of our Boolean comparisons. These operators are and, or, and not. We can use these to create more complex conditions.

17. **Combining conditions**
For example, if we wish to get only the rows for non-amazon stock later than April 1st, we can create two conditions, the first for the symbol, and the second the date. We then combine the conditions using the and operator, and use the combined condition as the argument to .loc[].

18. **Combining conditions**
The resulting DataFrame has only rows that match both conditions.

19. **Let's practice!**
Now, let's practice filtering DataFrames.