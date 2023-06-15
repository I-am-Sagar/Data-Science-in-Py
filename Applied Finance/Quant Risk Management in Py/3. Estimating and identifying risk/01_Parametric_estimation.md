1. **Parametric Estimation**
We can now manage portfolio risk using the VaR and CVaR risk measures and Modern Portfolio Theory. Next we'll learn how to estimate risk measures by fitting distributions to data.

2. **A class of distributions**
Generally, we do not know the exact form of the distribution of possible losses. But we may find it convenient to work with a class of distributions that best describes the loss distribution. Each member of a class is a function of the loss ‘x’ and has a set of parameters, which we call 'theta'. For example, a Normal distribution is a class of distributions, each with a different mean and standard deviation. These are the parameters of the distribution. Finding the 'best' parameter values given portfolio data is called parametric estimation. Once the optimal parameter values 'theta star' are found, the loss distribution can be described within the class of distributions.

3. **Fitting a distribution**
This kind of fitting usually involves trying to bend the shape of the class so that it minimizes some measurement of error. For example, the `fit()' method of Scipy's Normal distribution does this by selecting the best mean and standard deviation for error minimization. This provides a way to visually compare the fitted distribution and a histogram of the data. It also allows us to use statistical inference to measure goodness of fit.

4. **Goodness of fit**
Consider this histogram of portfolio losses. We would like to see how different parametric estimates fit this data. This is a visualization 'goodness of fit' test, using the histogram as the 'benchmark' representation.

5. **Goodness of fit**
We can use the 'scipy stats' Python library to create a Normal distribution object, 'norm', and then fit the data with the `fit()' method. In our example, we see that although the average of the data seems to be closely estimated, the overall shape of the Normal distribution is too 'wide', and not 'tall' enough.

6. **Goodness of fit**
Now let's try the Student's t-distribution. As you can see, the t-distribution fits the data better, being both 'taller' and 'narrower'. This means that the degrees of freedom of the T distribution, which is the number of independent observations, is estimated to be low. Although the T distribution provides a good fit, the data is still not quite right. In particular, the histogram is not symmetrical: it's a bit lopsided. We'll address this in a moment.

7. **Anderson-Darling test**
Sometimes a visualization will make it appear that a distribution is a good fit. How can we make this precise? The Anderson-Darling test is used to see how well a distribution fits the data. The null hypothesis is that the data are Normally distributed. This is rejected if the test statistic comes back larger than one or more critical values (just like a t-test from OLS). In Python, we use the test by first importing it from 'scipy stats'. Then we compute the test statistic on the actual loss data. The test returns the statistic and the associated critical values and significance levels. In this example, the test statistic of 11-point-04 is far larger than the 99% confidence level critical value of 1-point-081, indicating that the Normal distribution is not a good fit.

8. **Skewness**
Remember the lopsidedness of the data from our histogram? Skewness is the degree to which data is non-symmetrically distributed. Symmetric distribution classes, such as the Normal distribution,

9. **Skewness**
or the T distribution, cannot account for skewness.

10. **Skewness**
The Skewed Normal distribution is a generalization of the Normal distribution, and can be asymmetric. This is very useful for portfolio data, where (as we've seen) losses and gains may not be symmetrically distributed. The Skewed Normal distribution is available in 'scipy stats' as the 'skewnorm' object.

11. **Testing for skewness**
We can test for skewness in the data by seeing how far data are from being symmetric. In Python we test for skewness using 'skewtest' from 'scipy stats'. The null hypothesis is that there is no skewness, indicating that a symmetric distribution is appropriate. After importing the test, it is applied to the loss data. The results indicate both the test statistic value and its significance level. In our example, a test statistic of minus 7-point-78 has a more than 99-point-9% confidence level, showing that the data has statistically significant skewness. Parametric estimation using a Skewed Normal distribution might then be appropriate.

12. **Let's practice!**
Test your knowledge of parametric estimation for the Normal and Skewed Normal distributions in the following exercises. Good luck!