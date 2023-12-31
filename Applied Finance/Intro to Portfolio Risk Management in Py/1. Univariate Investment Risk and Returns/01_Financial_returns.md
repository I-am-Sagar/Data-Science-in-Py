1. **Financial returns**
Hello, and welcome to this course on Portfolio Risk Management in Python! I'm Dakota Wixom, and I'll be your instructor for this course.

2. **Course overview**
In this course, you'll learn how to analyze return distributions, build portfolios, identify factors driving portfolio returns, and even estimate potential losses. But before we get into portfolio investing, factor analysis, or risk management, it is essential to understand the fundamental properties of financial returns, which is what this chapter is all about.

3. **Investment risk**
To kick things off, let's first define the term "risk" itself. Financial risk can simply be thought of as a measure of the uncertainty of future returns. When analyzing returns, we can say that risk is essentially the dispersion or variance of those returns.

4. **Financial risk**
What I'm getting at is that financial risk has many different definitions, but they all hinge on two fundamental concepts: Returns and Probability.

5. **A tale of two returns**
Before we get ahead of ourselves, let's do a quick refresher on financial returns. Financial returns are generally derived from stock prices, and are expressed as percentages in decimal form. There are two common types of financial returns: discrete returns (also called simple returns), and log returns (also called continuous returns). For this course, you will be using mostly discrete returns at the daily frequency. Log returns are used for some advanced formulas and financial models in finance.

6. **Calculating stock returns**
There is a very simple formula to calculate simple returns, which is simply today's price minus yesterday's price, divided by yesterday's price. This gives you a percentage gain or loss for the day.

7. **Calculating log returns**
Log returns are actually pretty easy to calculate, too, but we can ignore them for the sake of this course. What is important to understand though is that log returns aggregate across time, while discrete returns aggregate across assets. Since you are building portfolios with multiple assets, discrete returns make the most sense to work with for this course.

8. **Calculating stock returns in Python**
In order to calculate returns, you're first going to need stock price data to work with. We will provide you with CSV files containing stock prices, and it's your job to read in that data and process it into a DataFrame. To accomplish all of this, you'll need to work with the Python module Pandas, which will come in handy for this course. Make sure to parse the dates, sort the values by date, and then set the index to the 'Date' column.

9. **Calculating stock Returns in Python**
Now that you've wrangled the data, calculating daily returns is as easy as calling the dot pct_change() method on the proper column. If you call the dot head() method on your returns, you'll notice that the very first period has an invalid return entry. This is because in the first period, there was no previous price to derive the return from.

10. **Visualizing return distributions**
In order to visualize the distribution of your daily returns, you're going to need to first import the matplotlib dot pyplot module. Remember how the first period had no return? You will need to call the dot dropna() method on your returns before passing them into the hist() function. Setting bins equal to a large number will spread out your plot, but a low number will cause a lack of resolution. If you set density equal to False, you will plot the frequency of returns rather than the probability density on the y-axis. Finally, call plt dot show() to display the plot.

11. **Let's practice!**
Got everything? Great, now let's try some examples.

