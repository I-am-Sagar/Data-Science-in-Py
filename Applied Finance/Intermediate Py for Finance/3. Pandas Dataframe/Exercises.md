### Question 1: Creating DataFrames

A security position is a record of ownership that includes the purchase price and date. This information is necessary if you want to calculate how much profit was made on a stock. You can have multiple positions of the same stock, if you purchase it multiple times. Use these positions of Apple stock to create DataFrames in this exercise:

| Sym |	Price |	Date |
| --- | --- | --- |
| APPL |	105.00 |	2015/12/31 |
| APPL |	117.05 |	2017/12/01 |
| APPL |	289.80 |	2019/12/27 |

**Instructions 1/3**

1. Create a dictionary with the exact column names holding the Apple data.
2. Create a DataFrame using the dictionary.

**Pre Code**

```py
# Create dict holding the data
data = {'____': ['APPL', 'APPL', 'APPL'],
        '____': [105.00, 117.05, 289.80],
        '____': ['2015/12/31', '2017/12/01', '2019/12/27']}

# Create DataFrame from the data
positions = pd.____(data=____)
print(positions)
```

**Ans.**

```py
# Create dict holding the data
data = {'Sym': ['APPL', 'APPL', 'APPL'],
        'Price': [105.00, 117.05, 289.80],
        'Date': ['2015/12/31', '2017/12/01', '2019/12/27']}

# Create DataFrame from the data
positions = pd.DataFrame(data=data)
print(positions)
```

**Instructions 2/3**

1. Create a list of dictionaries with the position data.
2. Create a DataFrame using the list.

**Pre Code**

```py
# Make list of dictionaries
data = [{'Sym': 'APPL', 'Price': 105.00, 'Date': '2015/12/31'},
        {'Sym': 'APPL', 'Price': 117.05, 'Date': '2017/12/01'},
        {'____': '____', '____': ____, '____': '____'}]

# Create DataFrame from the list
positions = ____.____(data=____)
print(positions)
```

**Ans.**

```py
# Make list of dictionaries
data = [{'Sym': 'APPL', 'Price': 105.00, 'Date': '2015/12/31'},
        {'Sym': 'APPL', 'Price': 117.05, 'Date': '2017/12/01'},
        {'Sym': 'APPL', 'Price': 289.80, 'Date': '2019/12/27'}]

# Create DataFrame from the list
positions = pd.DataFrame(data=data)
print(positions)
```

**Instructions 3/3**

1. Create a list of lists representing the positions data.
2. Define the column names.
3. Create a DataFrame from the data.

**Pre Code**

```py
# Create a list of lists
data = [['APPL', 105.00, '2015/12/31'],
        ['APPL', 117.05, '2017/12/01'],
        ['____', ____, '____']]

# Define the column names
columns = ['____', '____', '____']

# Create a DataFrame with the data and column names
df = pd.____(data=____, ____=____)
print(df)
```

**Ans.**

```py
# Create a list of lists
data = [['APPL', 105.00, '2015/12/31'],
        ['APPL', 117.05, '2017/12/01'],
        ['APPL', 289.80, '2019/12/27']]


# Define the column names
columns = ['Sym', 'Price', 'Date']

# Create a DataFrame with the data and column names
positions = pd.DataFrame(data=data, columns=columns)
print(positions)
```

### Question 2: Reading market history

Many data sources let you download data in the .csv file format. To understand a stocks performance over time it is useful to analyze its history. Imagine that you want to analyze the history of a stocks performance, looking at it closing prices for the last few months. The first thing you need to do is open the file as a DataFrame. The path to the .csv file containing the data is 'pcdg.csv'.

**Instructions**

1. Read the .csv file into a DataFrame.
2. Print the DataFrame.

**Pre Code**

```py
# Read the data
stocks = ____.____('____')

# Look at the data
print(____)
```

**Ans.**

```py
# Read the data
stocks = pd.read_csv('pcdg.csv')

# Look at the data
print(stocks)
```

### Question 3: Accessing using names

In this exercise, you will access data that tracks an account over time. This account consists of wealth from both cash and equities. The data is supplied in a DataFrame named ledger with the index set to dates, represented as strings. The data looks like this:

| |	Cash |	Securities |	Balance |
| --- | --- | --- | --- |
| 2020-10-01 |	0.0 |	-300.0	| 1222.0 |
| 2020-10-02 |	300.0 |	-200.0	| 1322.0 |
| 2020-10-03 |	-100.0 |	700.0 |	1922.0 |

**Instructions 1/3**

1. Use column and row names to select the balance as of October 2nd.
2. Select the balance as of October 3rd using names.

**Pre Code**

```py
# Select the Balance for October 2nd
print(ledger.loc['____','____'])

# Select the Balance for October 3rd
print(ledger.____['____','____'])
```

**Ans.**

```py
# Select the Balance for October 2nd
print(ledger.loc['2020-10-02','Balance'])

# Select the Balance for October 3rd
print(ledger.loc['2020-10-03','Balance'])
```

**Instructions 2/3**

1. Select cash and securities for October 3rd.
2. Select the balances for October 1st and 3rd.

**Pre Code**

```py
# Cash and Securities for October 3rd
print(ledger.____['2020-10-03', [____, ____]])
       
# Balance for October 1st and 3rd
print(ledger.____[____, 'Balance'])
```

**Ans.**

```py
# Cash and Securities for October 3rd
print(ledger.loc['2020-10-03', ['Cash', 'Securities']])
       
# Balance for October 1st and 3rd
print(ledger.loc[['2020-10-01', '2020-10-03'], 'Balance'])
```

**Instructions 3/3**

1. Use slicing to select all columns for October 1st.
2. Use slicing to select the balance for all dates.

**Pre Code**

```py
# All columns for October 1st
print(ledger.____['____', ____])

# Balance for all dates
print(____.____[____, '____'])
```

**Ans.**

```py
# All columns for October 1st
print(ledger.loc['2020-10-01', :])

# Balance for all dates
print(ledger.loc[:, 'Balance'])
```

### Question 4: Accessing using indexes

In this exercise, you will select and set stock positions using the numerical indexes of the rows and columns in a DataFrame. The provided DataFrame has this data:

| |	Symbol |	Purchased |	Quantity |	Price |
| --- | --- | --- | --- | --- |
| 0 |	AAPL |	2016-01-08 |	23 |	96.96 |
| 1 |	AAPL |	2018-09-07 |	50 |	221.30 |
| 2 |	AMZN |	2020-02-14 |	14 |	324.95 |

**Instructions 1/4**

1. Select the oldest price.
2. Select the newest symbol.

**Pre Code**

```py
# Cell first row, Price column
print(positions.iloc[____, ____])

# Cell last row, Symbol column
print(positions.____[____, ____])
```

**Ans.**

```py
# Cell first row, Price column
print(positions.iloc[0, 3])

# Cell last row, Symbol column
print(positions.iloc[2, 0])
```

**Instructions 2/4**

1. Use slicing to select the oldest two purchase dates.
2. Use slicing to select the most recent purchase and quantity values.

**Pre Code**

```py
# Oldest two purchase dates
print(positions.____[____, ____])

# Newest purchase and quantity
print(positions.____[____, ____])
```

**Ans.**

```py
# Oldest two purchase dates
print(positions.iloc[0:2, 1])

# Newest purchase and quantity
print(positions.iloc[2, 1:3])
```

**Instructions 3/4**

1. Set the quantity of the 2020 purchase to 15.

**Pre Code**

```py
# Set 2020 quantity
positions.iloc[____, ____] = ____

print(positions)
```

**Ans.**

```py
# Set 2020 quantity
positions.iloc[2, 2] = 15

print(positions)
```

**Instructions 4/4**

1. Set all of the quantity values to zero.

**Pre Code**

```py
# Set quantity
positions.____[____, ____] ____ ____

print(positions)
```

**Ans.**

```py
# Set quantity
positions.iloc[:, 2] = 0

print(positions)
```

### Question 5: Mean prices

When looking at stock prices it is useful to look at a prices not only over the course of multiple days, but at different points in the same data. In this exercise you are given historical data for a stock prices in a DataFrame named prices. The DataFrame has the columns OPEN, CLOSE, HI, and LOW. You are trying understand the trend of this stock's price by using the mean opening and closing prices. Is the mean opening price greater than the mean closing price?

1. Yes, the mean of the opening prices is higher than the mean of the closing ones.
2. No, the mean of the opening prices is lower than the mean of the closing ones.
3. No, the mean of the opening prices is equal to the mean of the closing ones.

**Ans.** 1

### Question 6: Median prices

There are times when the median is a better tool than the mean. Lets imagine that you are analyzing the stock data in the DataFrame prices again. You want to know if the stock's price is trending down by comparing the opening and closing prices. Remember the DataFrame has the columns OPEN, HI, LOW, and CLOSE.

**Instructions**

1. Calculate the median of the opening prices.
2. Calculate the median of the closing prices.
3. Compare the opening and closing medians to get the trend.

**Pre Code**

```py
# Get the median of the opening prices
med_open = ____.loc[:, '____'].____()

# Get the median of the closing prices
med_close = ____.____[:, '____'].____()

if ____ > ____:
    print("Trending down.")
```

**Ans.**

```py
# Get the median of the opening prices
med_open = prices.loc[:, 'OPEN'].median()

# Get the median of the closing prices
med_close = prices.loc[:, 'CLOSE'].median()

if med_open > med_close:
    print("Trending down.")
```

### Question 7: Creating new columns

Personal consumption expenditures (PCE) are a measurement of consumer consumption useful in judging the state and direction of the economy. Pretend that you are a financial analyst at an investment fund tasked with calculating PCE. PCE is the sum of consumption by consumers of durable goods (PCDG), non-durable goods (PCND), and services (PCESV). Let's calculate PCE using the list pcesv, the DataFrame pcnd, and PCDG from a CSV file.

**Instructions**

1. Create a column named PCESV from a list of values pcesv.
2. Create a column named PCND from the DataFrame pcnd.
3. Use the function .read_csv() to create a column named PCD' from the CSV file pcdg.csv.
4. Create a new column named PCE by adding other columns together.

**Pre Code**

```py
# Use the list pcesv to create the column PCESV
pce[____] = pcesv

# Use the DataFrame pcnd to create the column PCND
____ = pcnd

# Create column for PCDG using Pandas read_csv
pce['PCDG'] = pd.____('pcdg.csv', index_col='DATE')

# Create a column PCE by adding values from other columns
pce['PCE'] = pce['PCDG'] ____ pce['____'] + ____
pce.head()
```

**Ans.**

```py
# Use the list pcesv to create the column PCESV
pce['PCESV'] = pcesv

# Use the DataFrame pcnd to create the column PCND
pce['PCND'] = pcnd

# Create column for PCDG using Pandas read_csv
pce['PCDG'] = pd.read_csv('pcdg.csv', index_col='DATE')

# Create a column PCE by adding values from other columns
pce['PCE'] = pce['PCDG'] + pce['PCND'] + pce['PCESV']
pce.head()
```

### Question 8: Dropping columns from DataFrame

Sometimes your DataFrame has columns that you no longer need. It is often the case that you need to simplify a DataFrame by removing columns. Do you remember from the video which method you need to use to drop a row or a column?

Pretend that you wish to present the results of your PCE calculation to stakeholders at your company, without presenting the columns you used for the calculation. Drop the columns PCDG, PCND, and PCESV from the supplied DataFrame pce, leaving only the column PCE. The list columns_to_drop is provided.

**Instructions**

1. Print the columns of the pce DataFrame.
2. Create a new DataFrame from pce without the columns in the list columns_to_drop.
3. Print the columns of the new DataFrame.
4. Drop the columns in columns_to_drop from the DataFrame pce in place.

**Pre Code**

```py
columns_to_drop = ['PCDG', 'PCND', 'PCESV']

# Print the current columns of the DataFrame pce
____(pce.columns)

# Create new_pce by dropping columns_to_drop from pce
new_pce = pce.drop(columns=____)
# Print the columns of the new DataFrame
print(new_pce.____)

# Drop the columns in_place in the original DataFrame
pce.____(columns=columns_to_drop, inplace=____)

# Print the columns of the DataFrame pce
print(pce.columns)
```

**Ans.**

```py
columns_to_drop = ['PCDG', 'PCND', 'PCESV']

# Print the current columns of the DataFrame pce
print(pce.columns)

# Create new_pce by dropping columns_to_drop from pce
new_pce = pce.drop(columns=columns_to_drop)
# Print the columns of the new DataFrame
print(new_pce.columns)

# Drop the columns in_place in the original DataFrame
pce.drop(columns=columns_to_drop, inplace=True)

# Print the columns of the DataFrame pce
print(pce.columns)
```

### Question 9: Manipulating data with Pandas

You can combine data from different sources into a single DataFrame.

Imagine that you are tasked with calculating GDP to understand the health of the US economy. You have gathered the data you need from disparate sources in different formats.

You can calculate gross domestic product using the supplied DataFrames for personal consumption expenditures, government expenditures, gross private domestic investment, and net exports. The DataFrames ge, gpdi, ne, and pce are provided.

**Instructions**

1. Combine the supplied source DataFrames ge, gpdi, ne and pce in that order into a single new DataFrame.
2. Sum the values in each row to produce the GDP per year.

**Pre Code**

```py
# Combine the source DataFrames into one
gdp = pd.____([ge, gpdi, ____, ____], axis=1)

# Add the columns and create a new column with the result
gdp['GDP'] = gdp.____(np.sum, axis=1)
```

**Ans.**

```py
# Combine the source DataFrames into one
gdp = pd.concat([ge, gpdi, ne, pce], axis=1)

# Add the columns and create a new column with the result
gdp['GDP'] = gdp.apply(np.sum, axis=1)
```
<hr>