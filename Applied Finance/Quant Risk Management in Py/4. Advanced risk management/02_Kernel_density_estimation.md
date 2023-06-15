1. **Kernel density estimation**
We'll now augment our estimation toolkit with kernel density estimation, a flexible and powerful method of estimating the distribution of risk factors.

2. **The histogram revisited**
Up to now our risk factor distributions have been assumed (such as the Normal or T distribution), fitted (from, for example, parametric estimation or Monte Carlo simulation), or ignored (as with historical simulation). In each case, actual data can be summarized with a histogram. A histogram is not a distribution: but we would like a function to represent the histogram as a probability distribution (or density function). How can we do this? A middle ground between parametric estimation and ignoring the distribution is to filter the data so that they become smooth enough to represent a distribution. This can be done with non-parametric estimation, which does not assume a parametrized class of distributions (such as the Normal, Skewed Normal, or Student's t-distribution).

3. **Data smoothing**
The idea behind a filter is to smoothen out the 'bumps' of a histogram, so that a function can be fit to the histogram data.

4. **Data smoothing**
Suppose we have a bunch of observations of (say) portfolio losses. One by one

5. **Data smoothing**
they accumulate

6. **Data smoothing**
in nearby 'clusters', like histogram bins. We can create a function over portfolio losses by

7. **Data smoothing**
We can create a function over portfolio losses by picking a specific portfolio loss,

8. **Data smoothing**
picking a specific portfolio loss, looking at loss values nearby,

9. **Data smoothing**
and forming a kind of weighted average of the losses nearby that loss (including the specific loss itself). The choice of filter, or "kernel", tells us how to weight the specific value and the values nearby. You can think of the kernel as defining the "window" of values nearby, and how to average the values together.

10. **Data smoothing**
Moving the window to another portfolio value creates another weighted average.

11. **Data smoothing**
By doing this repeatedly, a kernel density estimate (KDE) function can be created over the entire range of observations.

12. **The Gaussian kernel**
A popular choice of window is the Gaussian kernel. This is a continuous kernel that puts the selected portfolio value at the center of a Normal distribution, and then weighs neighboring values according to how far away they are from the center. There are in general many kernels that can be used to fit a given set of observations. Kernel density estimation is extensively used in time series analysis, signal processing, and many other problem areas.

13. **KDE in Python**
We can use the 'scipy stats' library to generate a kernel density estimate of the distribution of losses for the investment bank portfolio from 2005 - 2010. First, import the `gaussian_kde()' function from 'scipy stats'. This is the Gaussian kernel density estimate function. Next, use `gaussian_kde()' on the losses, to generate the smoothed estimate of the loss distribution as the 'kde' object. This estimate can be visualized by plotting the `pdf()' of the ‘kde’ object, showing the shape of the resulting KDE distribution as fitted to the data.

14. **Finding VaR using KDE**
Once the kernel density estimate has been found, we can create our VaR risk estimate from the estimated probability distribution. To find the VaR, we first generate a sample of random draws from the estimated distribution using the `resample()' method. The sample size should be large to accurately reflect the estimate. Then we apply Numpy's `quantile()' function at a particular confidence level, say 99%, to generate the VaR estimate. A similar procedure as in the past can be used to compute the CVaR risk estimate. However, the Gaussian KDE object has no `expect()' method, so the integral in the expected value needs to be calculated manually. For the exercises, a special `expect()' method has been written for you, to assist in this computation, but keep in mind it is not generally available and isn't within the scope of the course.

15. **Let's practice!**
Kernel density estimation is widely used in data science, and you can gain experience with its use in the following exercises!

