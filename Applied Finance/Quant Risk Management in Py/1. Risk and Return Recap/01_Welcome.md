1. **Welcome!**
Greetings and welcome to Quantitative Risk Management in Python. My name is Jamsheed Shorish and I’ll be your host as we learn how to understand and manage risk: the impact of uncertainty on investment returns.

2. **About Me**
I’m a computational economist, specialising in asset pricing, cutting-edge financial technologies (or “fintech”), and applications of computational techniques to economics and finance. I'm an honorary associate professor at the Australian National University and a co-instructor of the "Economic Analysis of the Digital Economy". I'm also the CEO and Founder of Shorish Research, focusing on computational business applications.

3. **What is Quantitative Risk Management?**
Quantitative Risk Management is the study of quantifiable uncertainty. Uncertainty exists because future outcomes are unknown, and those outcomes may impact decisions that we make today. Risk management is the science of mitigating the impact of adverse outcomes. We quantify uncertainty by measuring risk. Measuring risk identifies factors that may create adverse outcomes in the future. This is like identifying the main causes of fire when creating fire insurance: we use things like historical causes of fire, as well as characteristics of houses that are prone to fire, in order to arrive at the best insurance possible. In this course we will quantify the factors that affect the risk of financial portfolios.

4. **Risk management and the Global Financial Crisis**
We will focus upon a tumultuous time period in human history: the “Great Recession” of 2007-2010, when trillions of dollars of growth and wealth were lost within a 3-year period. A large part of this catastrophe was the global financial crisis of 2007-2009. This was a period of large-scale changes in fundamental asset values, resulting in uncertainty and high asset returns volatility. Risk management was crucial in saving (or in some cases, failing to save) banks and private enterprises alike.

5. **Quick recap: financial portfolios**
Before exploring the global financial crisis in more detail, let's first recap our understanding of financial portfolio risks and returns. A financial portfolio is a collection of assets with uncertain future returns. Examples include stocks, bonds and foreign exchange holdings, or "forex". Other more complicated assets include stock options, which we’ll discuss later in Chapter 2. As mentioned, the challenge of risk management is to quantify risk. For financial portfolios, we quantify risk to be able to make optimal investment strategies that maximize a portfolio’s return, conditional upon a level of risk we can tolerate (known as the 'risk appetite').

6. **Quantifying return**
Recall that the return of a portfolio is the weighted sum of the returns of the assets within a portfolio. We can easily find this return by placing our asset price data into a Pandas DataFrame, such as ‘prices’, and then using the `pct_change()' method of the DataFrame to compute the return. The portfolio return is the dot product of the portfolio weights and the returns.

7. **Quantifying risk**
We quantify risk through the volatility of a portfolio’s return. Once we have the list of returns of a portfolio’s assets, we can calculate the volatility. This is typically done by first finding the covariance matrix of all of the assets, and annualizing by multiplying by the number of trading days (here 252).

8. **Quantifying risk**
Recall that the diagonal of the covariance matrix is the variance of the individual asset,

9. **Quantifying risk**
while the off-diagonal elements are the covariances between the assets.

10. **Portfolio risk**
To find the portfolio risk its weights have to be identified. The portfolio variance is a quadratic function of the weights given the covariance matrix, which can be computed in Python using the "At" operator. The variance is usually then transformed into the standard deviation, resulting in the portfolio's volatility. Both variance and standard deviation are used as measures of volatility.

11. **Volatility time series**
It can be useful to observe how portfolio volatility changes over time. We can create a 'window' of a fixed time period, such as a week or a month, using the `rolling()' Series method. Taking the standard deviation and annualizing results in a volatility time series that can be analyzed and plotted, to identify trends or possible extreme events. This will be discussed further in Chapter 4.

12. **Let's practice!**
In the practice exercises you’ll reacquaint yourself with these risk and return definitions, before we put them to use in the succeeding Chapters to actively engage in risk management. Let's go!
