1. **Visualization in Python**
Visualization is an important aspect of data analysis. The better you can "see" your data, the better you can gain insights from your data. Visualizations are also important to communicate your findings to others.

2. **Matplotlib: A visualization package**
The most popular package in python used for visualization is called matplotlib. You can make amazing visuals using matplotlib and it has a nice gallery that provides example code to build these images.

3. **matplotlib.pyplot - diverse plotting functions**
Within matplotlib, we'll be using the module called pyplot. Pyplot contains a collection of functions that are useful for plotting. It is a common practice to import the pyplot module as plt. To do this, you can use the command import matplotlib dot pyplot as plt.

4. **matplotlib.pyplot - diverse plotting functions**
Within pyplot, the plot() function takes inputs that describe the data to be plotted. These inputs can be lists or arrays. To display the plot, use the function show().

5. **Plotting with pyplot**
For example, let's assume we have two lists named months and prices. The months list contains the months of a year, and the prices list contains the consumer price index corresponding to each month. Here we use pyplot's plot() function to create a plot of these two lists by passing months as the first argument and prices as the second argument. Next, we use pyplot's show() function to display this plot. Let's take a look at the resulting plot.

6. **Plot result**
As you can see here, the plot function draws a line graph and the data in the list months is mapped to the x-axis and the data in the list prices is mapped to the y-axis.

7. **Red solid line**
We can provide additional arguments to the plot() function to customize the plot. For example, you can change the color of the line by setting the color argument to the string 'red'. This code results in the following plot.

8. **Plot result**
Now, what if you wanted a dashed red line instead of a solid red line?

9. **Dashed line**
You can accomplish this by adding the linestyle argument. To get a dashed line, set the linestyle argument to a string with two hyphens: '--'. Let's take a look at the resulting output.

10. **Plot result**
You can see that it is very easy to customize plots with pyplot.

11. **Colors and linestyles**
There are many colors and linestyles you can use in Matplotlib - here are just a few options.

12. **Adding Labels and Titles**
It's always a good practice to label your plots. You can use the xlabel(), ylabel() and title() functions to add x and y labels and the title to your plot, as shown here.

13. **Plot result**
This plot is looking really nice!

14. **Adding additional lines**
Often, you will want to compare multiple quantities by displaying them on the same plot. You can do this by using an additional plot() function. We've created another list of consumer price indices named prices_new. By adding one more call to the plot() function, we can add this list on our existing plot. We've also specified the color as green and the linestyle as dashed.

15. **Plot result**
The output of this code would result in a graph with two lines, a red one and a green one representing two sets of CPI. In the next lesson, we will see how to add a legend to the plots.

16. **Scatterplots**
In addition to line plots, you can also use matplotlib to plot a scatterplot. The scatter() function takes similar arguments as the plot() function. In this case, we will make a scatterplot of our months and prices lists using the scatter() function. Additionally, we also specify the color argument as red.

17. **Scatterplot result**
The resulting plot is a scatterplot with red markers.

18. **Let's practice!**
Now that you've been introduced to pyplot in matplotlib, let's give it a try on some financial data.