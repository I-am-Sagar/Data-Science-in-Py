1. **Portfolio analysis tools**
Let's explore portfolio analysis tools.

2. **Professional portfolio analysis tools**
Most portfolio managers spend a lot of time trying to understand what drives their portfolio's performance. In the last video, you've already seen how the Fama French model is used to the find main drivers of performance. Most professional managers have sophisticated in-house tools to help them analyze their portfolios. With those tools, they can easily break down their performance, this is called performance attribution, or test new strategies, this is called back-testing. In this video, you'll learn about publicly available tools to help you analyze your portfolio.

3. **Back-testing your strategy**
Let's talk about back-testing. Back-testing is the practice of running your investment strategy on historic data, to understand how it would have performed, if you would have traded it over that historic time period. It gives you a historical performance, from which you can calculate indicative risk and return numbers, for future returns. However, a word of warning: be very careful with extrapolating back-test results to the future. When a strategy works well on historic data, it is not guaranteed to work well on current and future data. The underlying markets can and will change, for example they can become more volatile. A good back-test is never a guarantee for strong future performance.

4. **Quantopian's pyfolio tool**
As mentioned, professional managers often use in-house tooling for performance attribution and back-testing. So what can we as hobbyists use? Well, a publicly available and incredibly useful tool for portfolio analysis is Quantopian's pyfolio tool. All of the things that we have covered so far in this course, can be calculated using pyfolio. For example pyfolio can give you with just a few lines of code, an extensive performance analysis, risk analysis, factor exposure analysis and performance attribution. You can also back-test your investment strategy with it. The only drawback with pyfolio I find, is that it is pretty strict in the format of data it can handle as input. Also, although you can install and run it on your local computer, it works best on their online platform.

1 Github: https://github.com/quantopian/pyfolio

5. **Performance and risk analysis in Pyfolio**
One of the most powerful analysis tools in pyfolio is the returns tear sheet. In order to start using pyfolio, make sure you have the package installed and imported. Pyfolio's return tear sheet needs to have a pandas series as input, so make sure your portfolio return data is in this format, and that the index is in datetime format. Then in one line of code, you can create the tear sheet. You can also distinguish between the back-test data, and live trading data, by adding a date on which you started live trading, like this.

6. **Pyfolio's tear sheet**
The output of the tear sheet is very detailed and long so I have shown only a few parts of the output here. In finance, a tear sheet provides a one-page summary of a portfolio, containing current and historic information on risk and returns. They are sometimes also referred to as Fund Fact Sheets. On the left here are all the different return numbers, most of which we've covered in the previous videos. You also get these nice plots of rolling volatility, Sharpe ratio and drawdowns, as shown on the right.

7. **Holdings and exposures in Pyfolio**
Pyfolio can also help you break down your portfolio's performance, with the performance attribution tools and industry exposure tool. The position tear sheet contains the information about exposures to factors such as industry and country. This is how to create an position tear sheet in pyfolio. The function takes the portfolio's returns, a sector map as defined here, and the positions we saw earlier.

8. **Exposure tear sheet results**
This is again only part of the output in the tear sheet, as the tear sheet provides very detailed information about the number of holdings, top holdings, which industry is overweight and underweight, etc. The outputs are always over the specified time period.

9. **Let's practice!**
Let's practice!