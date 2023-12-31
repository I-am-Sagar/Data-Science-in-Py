### Question 1: Equality across types

The equality operator == can be used to test if two variables have the same value. What is the result of using the equality operator to compare a variable closing_price, which holds the floating point value for a stocks closing price, to the variable closing_time, which holds a datetime object with the time of closing as a value?

1. True
2. False
3. A TypeError complaining about comparing different types
4. A warning message complaining about comparing different types

**Ans.** 2

### Question 2: Assignment and equality

When looking at someone's wealth, a distinction between cash and non-cash securities is important. Savings and checking accounts are cash securities. Stock positions are non-cash. Imagine that as part of balancing a client's wealth portfolio, you are asked to compare their cash and non-cash securities. The variable non_cash is provided with the value of the non-cash securities.

**Instructions**

1. Assign a value of 19.11 to the variable cash.
2. Check if cash and non_cash have the same value.
3. Assign to cash the value of non_cash.
4. Confirm that cash and non_cash are equal.

**Pre Code**

```py
# Assign a value to cash.
____ ____ ____

# Check if cash is equal to non-cash
print(____ ____ ____)

# Assign the value of cash to be equal non-cash
____ ____ ____

# Check if cash is equal to non-cash
print(____ ____ ____)
```

**Ans.**

```py
# Assign a value to cash.
cash = 19.11

# Check if cash is equal to securities
print(cash == non_cash)

# Assign the value of securities to cash
cash = non_cash

# Check if cash is equal to securities
print(cash == non_cash)
```

### Question 3: Comparing dividends

Dividends are payments made to stockholders, usually from profits that are not re-invested in a company. It is important to identify which stocks are paying higher dividends when analyzing how to balance stocks in a portfolio. Let's say that in your role analyzing a client's portfolio, you are tasked with comparing dividends from different holdings. The values of these dividends are provided in the variables d1 and d2.

**Instructions 1/2**

1. Find out if dividend d2 is greater than zero.
2. See if dividend d1 is greater than d2.

**Pre Code**

```py
# Check dividend is greater than zero
print(____ ____ ____)

# Is dividend 1 is greater than dividend 2?
print(____ ____ ____)
```

**Ans.**

```py
# Check dividend is greater than zero
print(d2 > 0)

# Is dividend 1 is greater than dividend 2?
print(d1 > d2)
```

**Instructions 2/2**

1. Check that dividend 1 is at least 100 units.
2. Check that dividend 1 is not more than dividend 2.

**Pre Code**

```py
# Check dividend 1 is at least 100
print(____ ____ ____)

# Check dividend 2 is at least as much dividend 1
print(____ ____ ____)
```

**Ans.**

```py
# Check dividend 1 is at least 100
print(d1 >= 100)

# Check dividend 2 is at least as much dividend 1
print(d1 <= d2)
```

### Question 4: Decisions with Boolean operations

Boolean operations are used in Python to make decisions. Imagine that you work as an analyst identifying accounts that might potentially participate in stock trades. You might use this information to advise qualifying clients on market moves. The variable is_investment_account is supplied. It is set to True if the given account includes stock positions as part of it's holdings. The supplied variable balance_positive is set to True if the account has a positive cash balance, which could be used to purchase securities.

**Instructions**

1. Print the value of the variable balance_positive.
2. Set the variable potential_trade to True if the account is an investment account with a positive balance.
3. Print the True if this is a potential trade.

**Pre Code**

```py
# Print the given variables
print(is_investment_account)
print(____)

# Decide if this account is cantidate for trading advice
potential_trade = is_investment_account ____ balance_positive

# Print if this represents a potential trade
print(____)
```

**Ans.**

```py
# Print the given variables
print(is_investment_account)
print(balance_positive)

# Decide if this account is cantidate for trading advice
potential_trade = is_investment_account and balance_positive

# Print if this represents a potential trade
print(potential_trade)
```

### Question 5: Assigning variables with Boolean operators

You can use the fact that and and or are short-circuit operators to assign objects to variables in intelligent ways. Pretend that you are deciding what actions you should take with a client's account based on what they entered in a web-form. Unfortunately, they could submit the form with this field empty, so you need to set a default action just in case. The supplied variable input_action has the contents submitted by the client. The supplied variable is_trading_day is True if today is a day that trades are possible.

**Instructions**

1. If your client entered an action, assign it to the variable action. If they entered nothing, use the default action "Hold".
2. Assign the action to the variable do_action if trades can be done today, otherwise assign it as False.
3. Print the action that should be done.

**Pre Code**

```py
# Assign a default action if no input
action = input_action ____ "Hold"

# Print the action
print(action)

# Assign action only if trades can be made
do_action = is_trading_day ____ action

# Print the action to do
____(____)
```

**Ans.**

```py
# Assign a default action if no input
action = input_action or "Hold"

# Print the action
print(action)

# Assign action only if trades can be made
do_action = is_trading_day and action

# Print the action to do
print(do_action)
```

### Question 6: Negating with Boolean operators

It is often the case that you need to combine Boolean operations to solve more complicated problems. Let's say that you need to know if you need to download the closing stock prices for today. You only want to do the operation if the markets have already closed. The closing prices are a list held in the provided variable closing_prices. The supplied variable market_closed is set to True once the markets close. Use Boolean operations and what you know about how objects evaluate in them to determine if you should download the data.

**Instructions**

1. Set the variable not_prices to True if you do not have closing prices for today.
2. Set the variable get_prices to True if the market is closed and you don't have closing prices yet.

**Pre Code**

```py
print(closing_prices)

# Assigning True if we need to get the prices
not_prices = ____ closing_prices

print(not_prices)

# Get prices if market is closed and we don't have prices
get_prices = ____ (market_closed ____ not_prices)

print(get_prices)
```

**Ans.**

```py
print(closing_prices)

# Assigning True if we need to get the prices
not_prices = not closing_prices

print(not_prices)

# Get prices if market is closed and we don't have prices
get_prices = not (market_closed and not_prices)

print(get_prices)
```

### Question 7: Control statements

An if statement consists of a controlling statement and a group of statements whose execution is controlled. What elements make up a control statement?

1. The keyword if, a series of statements with the same indentation, and a colon.
2. The keyword if, an expression which evaluates to True or False, and a colon.
3. The keyword if, an expression which evaluates to True or False, and a code block.

**Ans.** 2

### Question 8: Comparing sales and purchases

If statements let you branch your code to take different actions depending on the state of your data. Imagine you are working at a small firm trying to keep the number items sold in balance with those purchased. You are supplied with two lists, purchases, which contains items purchased, and sales, which contains items sold. Use if statements to compare the two lists.

**Instructions 1/3**

1. Assign the number of sales to the variable num_sales.
2. Check if the number of purchases is less than the number of sales.

**Pre Code**

```py
# Get number of purchases
num_purchases = len(purchases)
# Get number of sales
num_sales = ____(sales)

# Check if more sales than purchases
____ num_purchases < num_sales:
    print('buy more')
```

**Ans.**

```py
# Get number of purchases
num_purchases = len(purchases)
# Get number of sales
num_sales = len(sales)

# Check if more sales than purchases
if num_purchases < num_sales:
    print('buy more')
```

**Instructions 2/3**

1. Write a control statement to check if there were fewer sales than purchases.

**Pre Code**

```py
# Get number of purchases
num_purchases = len(purchases)
# Get number of sales
num_sales = len(sales)

# Check if fewer sales than purchases
____ ____ ____ ____ ____
    print('sell more')
```

**Ans.**

```py
# Get number of purchases
num_purchases = len(purchases)
# Get number of sales
num_sales = len(sales)

# Check if fewer sales than purchases
if num_sales < num_purchases :
    print('sell more')
```

**Instructions 3/3**

1. Check if both sales and purchases are empty.

**Pre Code**

```py
# Get number of purchases
num_purchases = len(purchases)
# Get number of sales
num_sales = len(sales)

# Check if both lists are empty
____ not (purchases ____ sales)____
    print('No sales or purchases')
```

**Ans.**

```py
# Get number of purchases
num_purchases = len(purchases)
# Get number of sales
num_sales = len(sales)

# Check if both lists are empty
if not (purchases or sales):
    print('No sales or purchases')
```

### Question 9: Branching with elif and else

elif and else statements let you extend your code to handle cases not handled by your initial control statement. In this exercise you will sort security transactions based on their stock symbol. You might do this to better understand how some popular stocks are bought and sold. You are provided with the variable trn which holds the transaction, and the empty lists appl, tsla, and amzn to hold sorted transactions.

**Instructions 1/3**

1. If the symbol is 'APPL', add it to the list appl

**Pre Code**

```py
# Get the symbol value
symbol = trn['symbol']

# Check if Apple stock
____ symbol ____ 'APPL'____
    appl.append(trn)
```

**Ans.**

```py
# Get the symbol value
symbol = trn['symbol']

# Check if Apple stock
if symbol == 'APPL':
    appl.append(trn)
```

**Instructions 2/3**

1. Write an statement to add 'TSLA' transaction to the list tsln.
2. Add the case that adds 'AMZN' transactions to the list amzn.

**Pre Code**

```py
# Get the symbol value
symbol = trn['symbol']

# Check if Apple stock
if symbol == 'APPL':
    appl.append(trn)
# Check if Tesla stock
____ ____ == 'TSLA':
    tsla.append(trn)
# Check if Amazon stock
____ ____ ____ 'AMZN'____
    amzn.append(trn)
```

**Ans.**

```py
# Get the symbol value
symbol = trn['symbol']

# Check if Apple stock
if symbol == 'APPL':
    appl.append(trn)
# Check if Tesla stock
elif symbol == 'TSLA':
    tsla.append(trn)
# Check if Amazon stock
elif symbol == 'AMZN':
    amzn.append(trn)
```

**Instructions 3/3**

1. If the symbol is any other company, print it.

**Pre Code**

```py
# Get the symbol value
symbol = trn['symbol']

# Check if Apple stock
if symbol == 'APPL':
    appl.append(trn)
# Check if Tesla stock
elif symbol == 'TSLA':
    tsla.append(trn)
# Check if Amazon stock
elif symbol == 'AMZN':
    amzn.append(trn)
# Handle other companies
_______
    print(symbol)
```

**Ans.**

```py
# Get the symbol value
symbol = trn['symbol']

# Check if Apple stock
if symbol == 'APPL':
    appl.append(trn)
# Check if Tesla stock
elif symbol == 'TSLA':
    tsla.append(trn)
# Check if Amazon stock
elif symbol == 'AMZN':
    amzn.append(trn)
# Handle other companies
else:
    print(symbol)
```


### Question 10: Breaking out of a for loop

You can use loops to perform operations which change depending on the data. For this exercise, you given a list of purchase transactions in the variable buys. You need to calculate the final balance of your client's account after the purchases have been made, but you do not want the account to have a negative balance. The initial account balance is provided in the variable balance.

**Instruction 1/2**

1. Create a loop which will iterate through the items in buys.
2. Subtract the cost of a purchase from the provided variable balance.

**Pre Code**

```py
# Loop through buys
____ buy ____ buys:
    print('Buying ' + buy['symbol'])
    new_balance = ____ - buy['total_cost']
    balance = new_balance

print(balance)
```

**Ans.**

```py
# Loop through buys
for buy in buys:
    print('Buying ' + buy['symbol'])
    new_balance = balance - buy['total_cost']
    balance = new_balance

print(balance)
```

**Instruction 2/2**

1. Check if the new balance would be negative.
2. Stop the iteration of the loop to prevent a negative balance.

**Pre Code**

```py
for buy in buys:
    print('Buying ' + buy['symbol'])
    new_balance = balance - buy['total_cost']
    ____ new_balance < 0:
        print('Unable to finish buys')
        ____
    balance = new_balance

print(balance)
```

**Ans.**

```py
for buy in buys:
    print('Buying ' + buy['symbol'])
    new_balance = balance - buy['total_cost']
    if new_balance < 0:
        print('Unable to finish buys')
        break
    balance = new_balance

print(balance)
```

### Question 11: Controlling loop execution

A typical pattern is to create a while loop with True as its condition and use a break statement to end it. In this exercise, your manager wants you to assemble a list of the five most recent years that the US had a positive trade gap. The dictionary nea is a mapping of datetimes to floats representing the net export for a given year. An empty list named surplus_years and a datetime named query_date are supplied.

**Instructions**

1. Create a loop with a condition that is always true.
2. Skip steps where net exports are less than zero.
3. Check the number of surplus years gathered.
4. Stop the loop once five years have been gathered.

**Pre Code**

```py
# Loop while true
while ____:
    net_exports = nea.get(query_date, -1)
    query_date = datetime(query_date.year - 1, 1, 1)
    # Skip if net exports are not positive
    if net_exports < 0:
        ----   
    surplus_years.append(query_date)
    # Check if 5 years have been collected
    ____ len(surplus_years) == 5:
        # Stop the loop
        ----
print(surplus_years)
```

**Ans.**

```py
# Loop while true
while True:
    net_exports = nea.get(query_date, -1)
    query_date = datetime(query_date.year - 1, 1, 1)
    # Skip if net exports are not positive
    if net_exports < 0:
        continue   
    surplus_years.append(query_date)
    # Check if 5 years have been collected
    if len(surplus_years) == 5:
        # Stop the loop
        break
print(surplus_years)
```

<hr>