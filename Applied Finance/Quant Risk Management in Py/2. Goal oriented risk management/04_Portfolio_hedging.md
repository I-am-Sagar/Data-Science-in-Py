1. **Portfolio hedging: offsetting risk**
Measuring risk using VaR and CVaR is part of risk management. Another part is using financial tools to offset or mitigate risk. We'll look at one such tool, hedging, in this video.

2. **Portfolio stability**
A risk measure such as VaR or CVaR indicates potential portfolio losses. These losses may still occur even after portfolio optimization has been performed, because of the volatility of the portfolio's risk factors. For large institutional investors, such as pension funds, portfolio stability is a key requirement because portfolio returns pay the income of individuals who have retired. US pension funds hold around 20 trillion dollars, roughly the amount of US output in a year.

3. **Rainy days, sunny days**
Suppose that you have invested in the stock of a company that sells sunglasses to vacation resorts all over the world. A risk factor for the stocks’s return might be the weather.

4. **Rainy days, sunny days**
In particular, when it rains, suppose the company is less valuable. The price of the stock falls, and so the portfolio value falls when it rains.

5. **Rainy days, sunny days**
Then you notice that another company, one which makes umbrellas, is more valuable when it rains.

6. **Rainy days, sunny days**
Investing in that company could reduce the risk to your original investment. The risk of rainy weather would be mitigated, and the overall impact of rain on your portfolio return would be reduced. The volatility of rain as a risk factor for sunglasses, in other words, is offset by investing in umbrellas.

7. **Hedging**
Using one or more assets to offset a risky position is called hedging. Hedging is one of the most important institutional investor techniques for risk management. By hedging a portfolio, an investor finds another return stream that moves in the opposite direction to the portfolio’s risk factor. Hedge portfolios are used in the aforementioned pension funds but also in currency trading, futures and derivatives trading, and mutual funds. In 2019 the hedge fund market was worth about 3-point-6 trillion dollars.

8. **Hedge instruments: options**
Hedging is often performed using derivatives to offset a risky asset position. One of the most basic derivatives is the European option. A European 'call' option gives the holder the right (but not the obligation) to purchase a stock for a fixed price X at a particular time M. A European 'put' option gives the holder the right (but not the obligation) to sell a stock for a fixed price X at a particular time M. The stock is called the 'underlying' of the option. The market price of the underlying is called the 'spot' price 'S'. The fixed price is called the ’strike’ price 'X' and the time 'M' is the 'maturity'.

9. **Black-Scholes option pricing**
The value of an option changes when the underlying asset price changes. If this change moves opposite to the price change, then a portfolio with the asset can be hedged. But how to value an option? Many factors, such as market efficiency, the underlying stock, and the risk-free interest rate all play a factor. Perhaps the most popular way is the Black-Scholes option pricing formula, from Fisher Black and Myron Scholes’ seminal work in 1973. To compute the Black-Scholes option price at a given time t, the spot price, strike price, time to maturity, risk-free interest rate and volatility are all needed.

1 Black, F. and M. Scholes (1973). "The Pricing of Options and Corporate Liabilities", Journal of Political Economy vol 81 no. 3, pp. 637–654.{{3}}

10. **Black-Scholes formula assumptions**
The Black-Scholes option pricing formula makes several assumptions about how markets work, and how the underlying stock price evolves. Although we won't go into the mathematical details, it is important to know that the pricing formula assumes that markets are well-functioning, that the stock price follows a particular statistical distribution, and that there are safe investment opportunities (such as bank deposits). You can get more information about the Black-Scholes option pricing formula by trying an online calculator, or by examining the source code for the function `black_scholes' (which is linked in the exercises).

11. **Computing the Black-Scholes option value**
To calculate the options value, a pre-generated function `black_scholes' is available. First, set the required spot and strike prices, the time to maturity (in fractions of a year), the risk-free interest rate, volatility, and the option type. The pricing formula will then yield the option value.

12. **Hedging a stock position with an option**
A portfolio made up of a single stock can be hedged by holding a European put option with the same underlying stock. The value of a put option goes up when the price of a stock goes down. This is because the option holder can sell at the strike price instead of suffering the price drop. The change in the option value is called the “delta” of the option. It is the derivative of the option value V with respect to the spot price S. By holding an amount of the option equal to one over the delta, changes in the price of the underlying stock can be offset. Delta neutrality is when the total change in the portfolio's value from a change in the portfolio's asset price is zero. The function `bs_delta' is used to compute the delta and there is a link to it in the exercises.

13. **Let's practice!**
In the exercises that follow you’ll practice using the Black-Scholes option pricing formula, and create a delta neutral hedged portfolio holding IBM stock. Good luck!

