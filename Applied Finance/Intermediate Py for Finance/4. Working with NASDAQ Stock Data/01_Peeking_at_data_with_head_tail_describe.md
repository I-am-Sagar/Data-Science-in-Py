1. **Peeking at data with head, tail, and describe**
Let's look at how to explore and gain insights from our data.

2. **Understanding your data**
When you first load data into a DataFrame, it is a good practice to take a look at it before you start manipulating it. This both ensures the data is loaded correctly and that you have a basic understanding of it's shape.

3. **First look at data**
The DataFrame we will use for this lesson contains a month's worth of closing prices for Apple stock.

4. **First look at data**
The index is the date of the close.

5. **First look at data**
The column Price is the closing price in dollars.

6. **First look at data**
the column Volume is the number of shares traded,

7. **First look at data**
and the column trend indicates whether the current price is higher or lower than that of the previous day. The data in the columns is of types float, integer, and object, which is the type Pandas uses for strings.

8. **Head**
The first thing I do with a new DataFrame is to take a peak at the first few rows. This is done using the .head() method. When you call .head() on a DataFrame it displays the first five rows. We can see that the values for these rows, and see that at least for the first five, they are ordered by date in a decreasing fashion.

9. **Head**
We can specify the number of rows returned

10. **Head**
by supplying an integer argument. Here we indicate we'd like to see three rows. And the first three rows are returned.

11. **Tail**
If you wish to see the bottom rows, you can use the .tail() method. It works the same way as .head(), but from the bottom. We can see here that our data goes back to February twenty eighth twenty twenty.

12. **Describe**
Now that you've taken a peek at the DataFrame, it often makes sense to look at a statistical summary of your data. The .describe() method offers such a summary. By default, .describe() will return summary statistics on all numerical columns, in this example the Price and Volume columns. For numerical columns, .describe() returns values for a count of the rows, the mean value across the rows, the standard deviation, the minimum value, percentiles for %25, %50, and %75, as well as the maximum value. We can see that in our data, the maximum price that Apple's stock reached was $302.74, and the minimum was $224.37.

13. **Include**
.describe() takes three option arguments, include, exclude, and percentiles. To see the summary statistics for the Trend column, specify 'object' as an value to include. You can see that different categories are returned depending on the column type. For an object type, the row count, the number of unique values, the top value, which has the highest count and the frequency of that value are calculated. In this case we can see that for the Trend column, 'Down' was the most frequent value, occurring fourteen out of twenty-one times.

14. **Include**
If you wish to see summaries for all columns, use the include argument with the value of 'all'. Summary statistics are calculated for all of the columns, with not a number (NaN), inserted where a statistic is not appropriate for the column type. For example, the mean cannot be calculated for the object-type column Trend, so it is set to not a number.

15. **Include**
If you want to choose multiple types, you can supply a list of types to return. Here we specified float and object, so the integer column, Volume, was skipped.

16. **Percentiles**
For numerical data, the default it to return percentiles for %25, %50, and %75. You can override this with the percentiles argument. It takes a list of percentiles you wish to see. Here we specify %10, %50, and %90. Which lets us see these percentiles closer to the edges of the data.

17. **Exclude**
The exclude argument works in the opposite way to include. It will return all column types, except those specified. Here we exclude columns of type float. This excludes our Price column, but includes all others.

18. **Let's practice!**
Lets practice looking at our data!