1. **Historical and Monte Carlo Simulation**
Now we'll examine two more estimation techniques widely used in risk management.

2. **Historical simulation**
It may be that losses are not distributed according to a well-defined distribution class. Historical simulation is very general. Historical simulation uses past data to create a simulation about the future loss. It makes no assumption about the loss distribution shape. If we have a vector of losses stretching back, say, 365 days, then we create a vector of 365 simulated losses from today onwards by using past losses as if they occurred today.

3. **Historical simulation in Python**
To compute the historically simulated VaR, we begin with the matrix of historical asset returns. We then find the portfolio's return. Converting returns to losses is easy: losses are just the negative of portfolio returns. Finally, we apply Numpy's 'quantile' function to compute the VaR at the desired confidence level. Although no distributional assumption is made, note that we do assume tomorrow's losses are distributed exactly the same way as historical losses, which may not be true!

4. **Monte Carlo simulation**
The generality of historical simulation is also its weakness. It may be not be true that the loss distribution is stable over time, especially during times of structural changes (such as the financial crisis). Monte Carlo simulation is a powerful technique that combines aspects of both parametric and historical simulation. Monte Carlo simulation starts with a particular distribution class for losses or risk factors. But Monte Carlo simulation uses the distribution to create a series of random draws. These simulate a path of losses over time. Once this is done for a single path, or run, the process is repeated with a new series of random draws, to create a set of runs. Each run generates a simulated loss. The VaR estimate is then computed as a quantile over these losses, so that the entire set of runs is treated as a distribution of losses.

5. **Monte Carlo simulation in Python**
Let's compute an example Value at Risk using Monte Carlo estimation, assuming a Normal distribution for portfolio losses. In the first step, we import the Normal distribution for our portfolio losses. We'll use this for our random draws. Next, we define the number of simulated random draws in each Monte Carlo run, called 'total steps'. In our example, we compute minute-by-minute losses to find a daily measure of the VaR. There are 1,440 minutes in a day, so we have 1,440 total steps in each run. The total number of runs should be enough to form a quantile for the VaR estimate. Generally, the larger the number of runs the better. A good minimum is 10,000 runs, as here, but larger simulations run into the millions of runs! Finally, we find the mean and standard deviation of actual portfolio losses to use in the Normal distribution. We could also use estimated values from parametric estimation.

6. **Monte Carlo simulation in Python**
The second step is to initialize the 'daily loss' vector, which keeps track of cumulative losses over the day. It has to be as long as the number of runs, 'N'. Then we create the Monte Carlo simulation run loop. For each run, the randomly generated losses over the tiny interval one over total_steps are drawn. Notice how the 'norm rvs()' method is used to draw from a standard Normal distribution. This is then scaled using 'sigma' and the time interval, and finally shifted using 'mu' and the time interval. This is a way to transform a standard Normal draw to match the loss distribution.

7. **Monte Carlo simulation in Python**
Once we have the loss vector for the run, we compute the daily loss by adding up all of the minute-by-minute losses. This gives us one simulated daily loss for each run, or in total 10,000 simulated daily losses. Finally, the entire vector of 10,000 simulated daily losses is treated as real data, and we apply Numpy's `quantile()' method, as we've done in the past, to find the 95% VaR Monte Carlo estimate.

8. **Simulating asset returns**
A more thorough (and common) approach is to simulate the returns for the individual assets in a portfolio, rather than just the portfolio's total return. This allows greater realism as each risk factor can contribute their own sample path. In addition, risk factors can be correlated: the covariance matrix can be used to compute asset returns in the simulation procedure. In the exercises, you'll perform this more common Monte Carlo simulation technique, by simulating the return of each asset in our investment bank portfolio.

9. **Let's practice!**
Historical and Monte Carlo simulation are part of the modern risk manager's risk estimation toolkit, and you'll work with both in the following exercises!