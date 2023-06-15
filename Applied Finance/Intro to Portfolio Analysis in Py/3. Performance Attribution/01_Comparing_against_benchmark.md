1. **Comparing against a benchmark**
Let's talk about comparing portfolios to a benchmark

2. **Active investing against a benchmark**
Most actively managed portfolios are fixed to a benchmark. The benchmark serves as a reference of what the investor otherwise could earn, aka it serves as an indication of opportunity costs. An example of a benchmark is the S&P500 stock index. The portfolio manager takes deliberate deviations from the benchmark, in order to beat it in terms of performance. In those cases, portfolio performance is always considered relative to its benchmark, and never as a total return. In this example you see clearly that the portfolio return in blue, follows the yellow benchmark, which is a Vanguard index closely, but is slightly better in terms of performance.

3. **Active return for an actively managed portfolio**
As I mentioned, performance of portfolios that are fixed to a benchmark should always be measured in terms of active returns, aka the relative performance to the benchmark, and not the total performance. The active return is simply calculated by taking the difference between the two. The higher the active return, the more performance you are getting relative to the benchmark. As you can imagine, in order to achieve a better than benchmark result, the portfolio manager needs to take strategic positions that deviate from the benchmark. Stocks that have a higher weight than the benchmark are overweight, and underweight are stocks that have less weight than the benchmark.

4. **Tracking error for an index tracker**
When we're talking about passive investment funds, also called index trackers, the performance is simply measured by tracking error. Tracking error also tells you how much the fund deviates from the benchmark, just like active return. However, notice the fundamental difference between the two. Passive funds try to mimic the benchmark as close as possible, so a low tracking error is desired.

5. **Active weights**
Let's talk more about active weights, these are the under- and overweight positions relative to the benchmark. In this example you see that the portfolio is overweight in the energy industry, and underweight in financials. It is common to look at active weights, also from a risk management position. Active weights that are very different from a benchmark, i.e. large deviations, are risky and will make it harder for the portfolio manager to follow the benchmark closely. Active weights therefore not only help you to explain performance, but also to assess risk.

1 Source: Schwab Center for Financial Research.

6. **Active return in Python**
Let's have a look at some data. Here we've taken the mean stock return over a year, as well as a snapshot of the portfolio weights and benchmark weights at the end of the year. For each stock we have added the industry classification, by using the Global Industry Classification System, or GICS.

1 Global Industry Classification System (GICS)

7. **Active return in Python**
Let's now calculate active return for a portfolio. We'll do it in a simple way by only using mean returns of the assets. First calculate the portfolio total return by multiplying the portfolio weights of the assets with their mean return. Sum it all up to get to the total return over the period. Repeat the steps for the benchmark with the benchmark weights. Then take the difference between the two.

8. **Active weights in Python**
Active weights are easily obtained if you use the pandas groupby function to group the stocks according to sector, and then summing the weights over the sectors, as shown in this example. Active weights can then be calculated by taking the summed portfolio industry weights minus the benchmark weights. Which looks like this. Let's give this a try in the exercises.

9. **Let's practice!**