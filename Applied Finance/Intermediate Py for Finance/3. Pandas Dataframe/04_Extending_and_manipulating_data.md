1. **Extending and manipulating data**
You have already seen how to create DataFrames and how to access the data they contain. Now let's look at extending and manipulating that data. Specifically, let us look at adding columns or rows to a DataFrame, and applying functions to a single column or whole DataFrame.

2. **PCE**
Personal consumption expenditures or PCE are a measurement of consumer consumption useful in judging the state and direction of the economy. PCE is the sum of consumption by consumers of durable goods,

3. **PCE**
non-durable goods,

1 By cactus cowboy
2 Open Clipart, CC0, https://commons.wikimedia.org/w/index.php?curid=64953673

4. **PCE**
and services.

1 By Smart Servier
2 https://smart.servier.com/, CC BY 3.0, https://commons.wikimedia.org/w/index.php?curid=74765623

5. **PCE**
Let's use DataFrames to calculate PCE.

1 By Clip Art by Vector Toons
2 Own work, CC BY-SA 4.0, https://commons.wikimedia.org/w/index.php?curid=65937611

6. **PCE - adding and removing columns**
We start with a DataFrame containing consumption of durable goods from 1929 to 1932.

7. **PCE - adding and removing columns**
To add a column of non-durable goods data, we can assign the new column data from a list.

8. **PCE - adding and removing columns**
And a new column is created with values from the data.

9. **PCE - adding and removing columns**
We can get the consumer service consumption from another DataFrame.

10. **PCE - adding and removing columns**
And assign its data to a new column in a similar way.

11. **PCE - adding and removing columns**
Now we have our three inputs used to calculate the PCE.

12. **PCE - adding and removing columns**
To calculate the PCE, simply add the three columns together. Pandas allows for doing operations across columns.

13. **PCE - adding and removing columns**
Now we have the results in the PCE column.

14. **PCE - adding and removing columns**
Now let's remove the input data. We can use the drop method to remove columns or rows. By specifying the axis as 1, we remove the named columns.

15. **PCE - adding and removing columns**
We use the inplace argument to change the current DataFrame rather than producing a new one.

16. **PCE - adding and removing rows**
You can use the data in another DataFrame,

17. **PCE - adding and removing rows**
to populate a new row

18. **PCE - adding and removing rows**
using the append method.

19. **PCE - adding and removing rows**
You can add multiple rows by calling the append method repeatedly. If we have a list of DataFrames, each one representing a row.

20. **PCE - adding and removing rows**
We can iterate through the list to add them as new rows.

21. **PCE - adding and removing rows**
You can use the drop method to remove rows in a similar fashion to dropping columns.

22. **PCE - adding and removing rows**
Notice that this method drops rows by default.

23. **PCE - adding and removing rows**
A more efficient way to add multiple rows is to use the concat function. First, add our pce DataFrame to a list of DataFrames with the new row data. Then call concat on the whole list

24. **PCE - adding and removing rows**
to produce a new DataFrame that includes all of the rows.

25. **PCE - operations on DataFrames**
You can perform operations on DataFrames. Here let's calculate the pce in Euros by multiplying the whole DataFrame by the conversion rate.

26. **PCE - operations on DataFrames**
You can see the output is a new DataFrame with the values converted to Euros.

27. **PCE - map**
An alternative way to change the data in a column is to use the map method. It takes a function and performs it on each cell in a column. Here we define a function to convert a Dollar value to Euros and pass map onto the PCE column.

28. **PCE - map**
The result shows the converted values.

29. Gross Domestic Product (GDP)
GDP is a measure of a nation's economic growth. It is calculated by adding personal consumption expenditures with government expenditures (spending by the government), gross private domestic investment (money invested by domestic companies), and net exports (the difference between exports and imports).

30. GDP - apply
We will use the DataFrame apply method to calculate GDP. While map does operations on the individual elements in a column, apply can perform operations across multiple columns or rows.

31. GDP - apply
Here we have a DataFrame with the inputs for GDP and the date as the index. We can calculate the GDP by summing up the rows using the apply method.

32. GDP - apply
The axis argument is used to indicate rows versus columns. We use the numpy sum function, and apply passes each row as an argument,

33. GDP - apply
summing the values from all of the columns per row to produce the GDP value per row. We use the result to make a GPD column.

34. Let's practice!
It's time to practice modifying DataFrame data.