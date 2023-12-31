1. **Random walks**
Just because stock market movements seem random, doesn't mean that you can't model the movements.

2. **Random walks**
Random, or stochastic, movements are apparent throughout nature. From tidal waves and earthquakes to crime, particle physics, and yes - of course - the stock market, you can use mathematics to predict the future and simulate possible outcomes. Of course, there is always going to be a measure of uncertainty to most of these examples, and especially in finance - but the process is still incredibly useful. There's a surprising amount of crossover between different stochastic methods for fields ranging from geophysics and quantum physics to biology and even sociology. This is why quants are often referred to as the rocket scientists of Wall Street - because sometimes they actually are! And nowadays no quant is worth his or her salt without programming tools such as Python.

3. **Random walks in Python**
Now, in Python, we will use the normal distribution as a starting point for our simulations. You can grab the mean and volatility, or standard deviation, from historical stock returns like we did for parametric VaR, and for this simulation we will need a starting stock price S0 and a forecast period, T, of 252 days in this example. First, we simulate 252 random samples from a normal distribution with the desired mean and volatility, adding 1 to turn them into multiplicative factors before taking the cumulative product and then multiplying by the starting stock value S0. That's it! That's a random walk simulation of a stock over the course of one year! Run these lines again and you will get a completely different outcome.

4. **Monte Carlo simulations**
So then what exactly is a Monte Carlo simulation? Since one random simulation won't suffice for an accurate estimate of anything, you can repeat the simulation hundreds, thousands, or even millions of times to create a massive range of possible outcomes - a Monte Carlo simulation. You can then study these ranges of outcomes in the same way that you studied historical values to compute historical value at risk, for example. The only difference is that you can create as many simulations as you want, and tweak them to have the characteristics you desire.

5. **Monte Carlo VaR in Python**
So we'll do exactly this! Throw the entire process into a for loop, appending the random simulations to an object at each iteration. Finally, use the np dot percentile function to calculate VaR 95 as before. Now run the process again, and you will compute an entirely different VaR(95)! To get more stable and accurate estimates, crank up the number of simulations - but be aware of the computation time. That's the power of Monte Carlo simulations! Of course, you can build incredibly complex Monte Carlo simulations for everything from insurance models and interest rates to stock prices and intraday portfolio movements.

6. **Let's practice!**
Now it's your turn to build your first Monte Carlo simulation!