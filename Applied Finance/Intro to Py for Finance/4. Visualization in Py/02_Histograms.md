1. **Histograms**
Histograms are one of the most common graphs used to display numeric data as they can quickly tell you the distribution of your data.

2. **Why histograms for financial analysis?**
In finance, some examples where you might see histograms being used are for economic indicators, stock returns, and commodity prices. In this histogram, you can see that most returns are concentrated around $100. This symmetrical shape of the data is typical for a normal distribution.

3. **Histograms and Data**
Histograms have several advantages: They can quickly tell you the shape and distribution of your data. They can also tell you if there is a lot of variability in your data. Finally, they can quickly identify abnormal data points or outliers in your data.

4. **Histograms and matplotlib.pyplot**
In pyplot, you can plot a histogram using the hist() function. The required argument to this hist() function is the list or array for which you want to generate the histogram. You can also pass the bins argument which is used to specify the number of bins in the histogram. In this example, we have a histogram from a list of consumer price indices over the course of a year. It has 3 bins or 3 ranges of prices for which we are displaying the frequency of occurences of those consumer price indices. What would happen if we changed this histogram to having 6 bins?

5. **Changing the number of bins**
As you can see here, when there are more bins, the number of observations in each bin decreases as the bindwidth decreases.

6. **Normalizing histogram data**
At times, you may want to know the relative frequency or the percentage of observations (rather than frequency counts). You can do this by adding an additional argument to the hist() function. To normalize the frequency to one, you add the argument normed = 1. Now, on the y axis instead of the number of occurences of a price index range, we have the percentage of the data that is represented in that price index range.

7. **Layering histograms on a plot**
It is possible that you may want to compare two histograms. Let's take a look at two lists of consumer price indices, prices (from our previous plot) and prices_new. To plot the data in these two lists as two separate histograms, we can use the histogram() function on each list sequentially. Remember, we can also add the argument normed to create normalized histograms for each dataset.

8. **Histogram result**
The resulting histogram looks like this. Note that the two histgrams overlap each other. If you would like to improve this plot, you can use another argument to change the transparency of histograms.

9. **Alpha: Changing transparency of histograms**
To do this, you can add the argument, alpha, to the hist() function. The alpha argument adjusts the transparency of each histogram plot and in this case, sets it to 0.5 or 50% for both histograms. We then use the show() function to display the output of this code, and we'd see the following output...

10. **Histogram result**
You can see both histograms more clearly now. It would also be useful to add a legend to differentiate the two histograms.

11. **Adding a legend**
To add a legend, the first thing we'll do is add specific labels to each hist() function using the argument label. We added a label "prices 1" to the histogram function associated with the list prices and a label "prices New" to associate with the histogram of the list price_new. We'll add the legend corresponding to these labels to the plot with with the legend() function.

12. **Histogram result**
And voila, here is a plot with two histograms and a legend based on the labels we provided.

13. **Let's practice!**
Visualizations bring data to life -- let's give you a chance to try them out with some exercises!