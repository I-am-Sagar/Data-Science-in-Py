1. **A closer look at the sectors**
Now that you have successfully calculated the price to earnings ratios of all companies within the S&P 100, let's look at sector specific trends.

2. **Your mission**
First, we will need to subset sector-specific datasets from the larger S&P dataset. Let's review how we can filter out specific information from a larger array.

3. **Step 1: Create a boolean filtering array**
Remember that boolean arrays can be used to manipulate other arrays. To create a boolean array, you can perform a conditional test as shown here. This conditional test is performed on each element of the array and a boolean result is returned in an array. This boolean array can then be used for filtering. Let's see how we would use this array to filter stock prices greater than 150.

4. **Step 2: Apply filtering array to subset another array**
Once you have your boolean array, you can use it on another array to select specific elements. Let's look here at line 3. You can see how we used filter_array to subset elements from stock_prices. In this case study, you will need to use filtering arrays to subset P/E ratios that are associated with specific sectors in the S&P 100.

5. **Step 3: Summarize P/E ratios**
Once you subset the P/E ratios for specific sectors, you can use numpy functions to calculate their average and standard deviation.

6. **Let's practice!**
Now that you have reviewed a little, let's continue with the case study!