1. **Plotting data**
Now it's time to look at visualizing your data with plots.

2. **Look at your data**
Visualizing your data is an important tool both to help you understand that data, and to communicate your findings to others. Often relationships between columns can be discovered by creating a plot between them.

3. **Introducing the data**
For this lesson, we will use a historical data set of stock prices for the company Exxon over one year and five year periods.

4. **Introducing the data**
We have columns for the date, the high price, the volume of shares traded, and the name of the month. Our index is the row number.

5. **Matplotlib**
The core library that most 2D plotting in Pandas uses is matplotlib. While this library is very powerful, it has a steep learning curve, so other libraries have been built on top of it. Pandas DataFrames have a simplified interface to matplotlib through the .plot() method.

6. **Line plot**
To create a simple line plot, simply supply the columns to use for the x and y axes. Here we will use the date as the x axis and the high price as the y axis.

7. **Line plot**
You can see with this simple method, we are able to produce a line graph showing the price fluctuations by date. You might want to use a plot like this to detect seasonal patterns in a stock's price. It is easy to see the trend of this stock's price, but the labels for our Date column are a bit hard to read.

8. **Rotate**
The .plot() method offers a lot of optional parameters. One is 'rot', which is the rotation of the labels. So if we want to rotate our labels by 90 degrees, we supply set the rot to 90.

9. **Rotate**
And we can see that our date labels are now much easier to read.

10. **Title**
If you are creating a plot to present to others, you can give it a title. The title parameter accepts a string argument.

11. **Title**
That string is then used as the plot title.

12. **Index**
If we leave out the x argument, the index is used for the x axis. Here we set the index to the 'Date', and then use it to create our plot.

13. **Index**
And we see that the date is still used for our x-axis.

14. **Plot types**
The default type of plot produced by the plot() method is a line plot. But there are many other plot types available. These are line plots, bar plots, horizontal bar plots, histograms, box plots, kernel density estimation plots, density plots, area plots, pie plots, scatter plots, and hexbin plots. Lets look at examples of a bar plot and a histogram.

15. **Bar**
To specify a plot type other than line, use the 'kind' parameter. Here we set kind to 'bar', and create a plot of volume by month.

16. **Bar**
Bar charts are a great way to visualize data by category. Here we can easily see which months saw the greatest trading volume in 2018.

17. **Hist**
A histogram is a great way to see the distribution of different values. If we want to look at the distribution of the price over our data, we set the y axis to our high price and the kind to 'hist' for histogram.

18. **Hist**
We can see that for this time period the price of the stock was close to $85 more than any other price.

19. **Let's practice!**
Let's practice plotting from DataFrames.