### Question 1: Growth and rate of return

Growth and Rate of Return are two concepts that are ubiquitous throughout the financial world. Recall that the cumulative returns from investing $100 in an asset that grows at 5% per year, over a 2 year period can be calculated as: `100*(1+0.05)**2`.

**Instructions**

1. Calculate the future value (cumulative return) of a $100 investment which grows at a rate of 6% per year for 30 years in a row and assign it to future_value.

**Pre Code**

```py
# Calculate the future value of the investment and print it out
future_value = ____
print("Future Value of Investment: " + str(round(future_value, 2)))
```

**Ans.**

```py
# Calculate the future value for the first investment
future_value = 100*(1 + 0.06)**(30)
print("Future Value of Investment: " + str(round(future_value, 2)))
```

### Question 2: Compound interest

As you saw in the previous exercise, both time and the rate of return are very important variables when forecasting the future value of an investment.

Another important variable is the number of compounding periods, which can greatly affect compounded returns over time.

**Instructions 1/3**

1. Calculate the value of a $100 investment which grows at a rate of 6% per year for 30 years in a row compounded once per year and assign it to investment_1.

**Pre Code**

```py
# Predefined variables
initial_investment = 100
growth_periods = 30
growth_rate = 0.06

# Calculate the value for the investment compounded once per year
compound_periods_1 = ____
investment_1 = ____
print("Investment 1: " + str(round(investment_1, 2)))
```

**Ans.**

```py
# Predefined variables
initial_investment = 100
growth_periods = 30
growth_rate = 0.06

# Calculate the value for the investment compounded once per year
compound_periods_1 = 1
investment_1 = initial_investment*(1 + growth_rate / compound_periods_1)**(compound_periods_1*growth_periods)
print("Investment 1: " + str(round(investment_1, 2)))
```

**Instructions 2/3**

1. Calculate the value of the same investment, but compounded quarterly and assign it to investment_2.

**Pre Code**

```py
# Predefined variables
initial_investment = 100
growth_periods = 30
growth_rate = 0.06

# Calculate the value for the investment compounded once per year
compound_periods_1 = 1
investment_1 = initial_investment*(1 + growth_rate / compound_periods_1)**(compound_periods_1*growth_periods)
print("Investment 1: " + str(round(investment_1, 2)))

# Calculate the value for the investment compounded quarterly
compound_periods_2 = ____
investment_2 = ____
print("Investment 2: " + str(round(investment_2, 2)))
```

**Ans.**

```py
# Predefined variables
initial_investment = 100
growth_periods = 30
growth_rate = 0.06

# Calculate the value for the investment compounded once per year
compound_periods_1 = 1
investment_1 = initial_investment*(1 + growth_rate / compound_periods_1)**(compound_periods_1*growth_periods)
print("Investment 1: " + str(round(investment_1, 2)))

# Calculate the value for the investment compounded quarterly
compound_periods_2 = 4
investment_2 = initial_investment*(1 + growth_rate / compound_periods_2)**(compound_periods_2*growth_periods)
print("Investment 2: " + str(round(investment_2, 2)))
```

**Instructions 3/3**

1. Calculate the value of the same investment, but compounded monthly and assign it to investment_3.

**Pre Code**

```py
# Predefined variables
initial_investment = 100
growth_periods = 30
growth_rate = 0.06

# Calculate the value for the investment compounded once per year
compound_periods_1 = 1
investment_1 = initial_investment*(1 + growth_rate / compound_periods_1)**(compound_periods_1*growth_periods)
print("Investment 1: " + str(round(investment_1, 2)))

# Calculate the value for the investment compounded quarterly
compound_periods_2 = 4
investment_2 = initial_investment*(1 + growth_rate / compound_periods_2)**(compound_periods_2*growth_periods)
print("Investment 2: " + str(round(investment_2, 2)))

# Calculate the value for the investment compounded monthly
compound_periods_3 = ____
investment_3 = ____
print("Investment 3: " + str(round(investment_3, 2)))
```

**Ans.**

```py
# Predefined variables
initial_investment = 100
growth_periods = 30
growth_rate = 0.06

# Calculate the value for the investment compounded once per year
compound_periods_1 = 1
investment_1 = initial_investment*(1 + growth_rate / compound_periods_1)**(compound_periods_1*growth_periods)
print("Investment 1: " + str(round(investment_1, 2)))

# Calculate the value for the investment compounded quarterly
compound_periods_2 = 4
investment_2 = initial_investment*(1 + growth_rate / compound_periods_2)**(compound_periods_2*growth_periods)
print("Investment 2: " + str(round(investment_2, 2)))

# Calculate the value for the investment compounded monthly
compound_periods_3 = 12
investment_3 = initial_investment*(1 + growth_rate / compound_periods_3)**(compound_periods_3*growth_periods)
print("Investment 3: " + str(round(investment_3, 2)))
```

### Question 3: Discount factors and depreciation

Unfortunately, not everything grows in value over time.

In fact, many assets depreciate, or lose value over time. To simulate this, you can simply assume a negative expected rate of return.

**Instructions 1/3**

1. Calculate the future value of a $100 investment that depreciates in value by 5% per year for 10 years and assign it to future_value.

**Pre Code**

```py
# Calculate the future value
initial_investment = 100
growth_rate = ____
growth_periods = ____
future_value = ____
print("Future value: " + str(round(future_value, 2)))
```

**Ans.**

```py
# Calculate the future value
initial_investment = 100
growth_rate = -0.05
growth_periods = 10
future_value = initial_investment*(1 + growth_rate)**(growth_periods)
print("Future value: " + str(round(future_value, 2)))
```

**Instructions 2/3**

1. Calculate the discount factor of the investment and assign it to discount_factor.

**Pre Code**

```py
# Calculate the future value
initial_investment = 100
growth_rate = -0.05
growth_periods = 10
future_value = initial_investment*(1 + growth_rate)**(growth_periods)
print("Future value: " + str(round(future_value, 2)))

# Calculate the discount factor
discount_factor = ____
print("Discount factor: " + str(round(discount_factor, 2)))
```

**Ans.**

```py
# Calculate the future value
initial_investment = 100
growth_rate = -0.05
growth_periods = 10
future_value = initial_investment*(1 + growth_rate)**(growth_periods)
print("Future value: " + str(round(future_value, 2)))

# Calculate the discount factor
discount_factor = 1/((1 + growth_rate)**(growth_periods))
print("Discount factor: " + str(round(discount_factor, 2)))
```

**Instructions 3/3**

1. Derive the initial value of the investment using the future value and the discount factor and assign it to initial_investment_again.

**Pre Code**

```py
# Calculate the future value
initial_investment = 100
growth_rate = -0.05
growth_periods = 10
future_value = initial_investment*(1 + growth_rate)**(growth_periods)
print("Future value: " + str(round(future_value, 2)))

# Calculate the discount factor
discount_factor = 1/((1 + growth_rate)**(growth_periods))
print("Discount factor: " + str(round(discount_factor, 2)))

# Derive the initial value of the investment
initial_investment_again = ____
print("Initial value: " + str(round(initial_investment_again, 2)))
```

**Ans.**

```py
# Calculate the future value
initial_investment = 100
growth_rate = -0.05
growth_periods = 10
future_value = initial_investment*(1 + growth_rate)**(growth_periods)
print("Future value: " + str(round(future_value, 2)))

# Calculate the discount factor
discount_factor = 1/((1 + growth_rate)**(growth_periods))
print("Discount factor: " + str(round(discount_factor, 2)))

# Derive the initial value of the investment
initial_investment_again = future_value * discount_factor
print("Initial value: " + str(round(initial_investment_again, 2)))
```

### Question 4: Present value

Luckily for you, there is a module called numpy which contains many functions which will make your life much easier when working with financial values.

The .pv(rate, nper, pmt, fv) function, for example, allows you to calculate the present value of an investment as before with a few simple parameters:

* rate: The rate of return of the investment
* nper: The lifespan of the investment
* pmt: The (fixed) payment at the beginning or end of each period (which is 0 in our example)
* fv: The future value of the investment

You can use this formula in many ways. For example, you can calculate the present value of future investments in today's dollars.

**Instructions**

1. Import numpy as np.
2. Using NumPy's .pv() function, compute the present value of an investment which will yield $10,000 15 years from now at an inflation rate of 3% per year and assign it to investment_1.
3. Compute the present value of the same investment, but with a time horizon of only 10 years and an inflation rate of 5%, assigning it to investment_2.

**Pre Code**

```py
# Import numpy as np
____

# Calculate investment_1
investment_1 = ____(rate=____, nper=____, pmt=____, fv=10000)

# Note that the present value returned is negative, so we multiply the result by -1
print("Investment 1 is worth " + str(round(-investment_1, 2)) + " in today's dollars")

# Calculate investment_2
investment_2 = ____
print("Investment 2 is worth " + str(round(-investment_2, 2)) + " in today's dollars")
```

**Ans.**

```py
# Import numpy as np
import numpy as np

# Calculate investment_1
investment_1 = np.pv(rate=0.03, nper=15, pmt=0, fv=10000)

# Note that the present value returned is negative, so we multiply the result by -1
print("Investment 1 is worth " + str(round(-investment_1, 2)) + " in today's dollars")

# Calculate investment_2
investment_2 = np.pv(rate=0.05, nper=10, pmt=0, fv=10000)
print("Investment 2 is worth " + str(round(-investment_2, 2)) + " in today's dollars")
```

### Question 5: Future value

The numpy module also contains a similar function, .fv(rate, nper, pmt, pv), which allows you to calculate the future value of an investment as before with a few simple parameters:

* rate: The rate of return of the investment
* nper: The lifespan of the investment
* pmt: The (fixed) payment at the beginning or end of each period (which is 0 in our example)
* pv: The present value of the investment

It is important to note that in this function call, you must pass a negative value into the pv parameter if it represents a negative cash flow (cash going out). In other words, if you were to compute the future value of an investment, requiring an up-front cash payment, you would need to pass a negative value to the pv parameter in the .fv() function.

**Instructions**

1. Using NumPy's .fv() function, calculate the future value of a $10,000 investment returning 5% per year for 15 years and assign it to investment_1.
2. Calculate the future value of a $10,000 investment returning 8% per year for 15 years and assign it to investment_2.

**Pre Code**

```py
import numpy as np

# Calculate investment_1
investment_1 = ____(rate=____, nper=____, pmt=0, pv=____)
print("Investment 1 will yield a total of $" + str(round(investment_1, 2)) + " in 15 years")

# Calculate investment_2
investment_2 = ____
print("Investment 2 will yield a total of $" + str(round(investment_2, 2)) + " in 15 years")
```

**Ans.**

```py
import numpy as np

# Calculate investment_1
investment_1 = np.fv(rate=0.05, nper=15, pmt=0, pv=-10000)
print("Investment 1 will yield a total of $" + str(round(investment_1, 2)) + " in 15 years")

# Calculate investment_2
investment_2 = np.fv(rate=0.08, nper=15, pmt=0, pv=-10000)
print("Investment 2 will yield a total of $" + str(round(investment_2, 2)) + " in 15 years")
```

### Question 6: 

**Instructions**



**Pre Code**

```py

```

**Ans.**

```py

```

### Question 7: 

**Instructions**



**Pre Code**

```py

```

**Ans.**

```py

```

### Question 8: 

**Instructions**



**Pre Code**

```py

```

**Ans.**

```py

```

### Question 9: 

**Instructions**



**Pre Code**

```py

```

**Ans.**

```py

```

### Question 10: 

**Instructions**



**Pre Code**

```py

```

**Ans.**

```py

```
