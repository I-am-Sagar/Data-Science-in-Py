1. **Accessing Data**
One of the many strengths of Pandas DataFrames is the ability to access your data either as an individual value, a column, a row, or as another DataFrame. Let's look at some ways to do this.

2. **Account Balance**
When working in the financial industry, there is often data that represents the idea of a client's account balance. This could be the balance of a savings account, a targeted purchase account, funds available for re-investment in a securities account, or any other account representing wealth.

3. **Introducing lesson data**
This is the data we will use for this lesson. It represents client accounts and has columns to identify the holding bank, the account number, and the current account balance. We have named our indexes 'a','b','c' and put this data into a DataFrame, named 'accounts'.

4. **Access column using brackets**
To access a column of our DataFrame, we can use a bracket syntax similar to what we have seen with lists and dictionaries. Put the name of the column, as a string, in brackets following the DataFrame name.

5. **Access column using brackets**
And the column, with its values and index, is returned.

6. **Access column using dot-syntax**
If the column you wish to access does not contain white space or dashes,it will be added as an attribute to the DataFrame. You can also access it using dot-syntax.

7. **Access multiple columns**
You can access multiple columns at once by supplying a list of names.

8. **Access multiple columns**
This gives you a DataFrame with only the columns requested. Here we requested the bank code and account number columns.

9. **Access rows using brackets**
The bracket syntax for Pandas DataFrames is overloaded - it has different functions depending on the input. You can use a slice argument to return a range of rows. The slice is just like the slice you would use with a list. It comprises a colon which can be preceded and/or followed by a integer. These integers describe the rows to select.

10. **Access rows using brackets**
The zero indicates we start with the first row, and the two specifies going up to, but not including the third row. Remember that Python is zero-indexed, so 2 is the third item.

11. **Access rows using brackets**
You can also specify rows using a list of Booleans.

12. **Access rows using brackets**
Here we fetch the first and last row, skipping the middle by passing a False value.

13. **loc and iloc**
The bracket and dot syntax methods are convenient for accessing data during exploration, but are not very efficient with large data sets. The DataFrame methods loc and iloc are more efficient and are the recommended way to access data in large data sets. The loc method uses names and the iloc uses positions.

14. **loc**
You can access a row by passing its name to loc in square brackets.

15. **loc**
To get multiple rows, you can pass in a list of row names, a list of Boolean values, or a slice based on the row names. In these examples we access the rows 'a' and 'c' using names and Booleans.

16. **Columns with loc**
You can specify columns by supplying a second argument. This can be a column name, a list of column names, a list of Booleans, or a slice based on column names. Note that when you slice using names, the last name is included, unlike with numbers.

17. **Columns with loc**
The returned value will reflect the rows and columns selected.

18. **Columns with loc**
Here we selected all of the rows and two of the columns.

19. **iloc**
The iloc method works in a similar way to loc, but with index and column positions rather than names.

20. **iloc**
Here we select the first two rows using a slice,

21. **iloc**
and the first and last columns using a list.

22. **Setting a single value**
We can use the same syntax we used to access values when updating them. If we specify a single row and column, we can set a single value.

23. **Setting a single value**
Here we have set the balance of row 'a' to zero.

24. **Setting multiple values**
Or you can set multiple cells to the same value at once by using any of multi-row and multi-column ways we have seen. Here we use slices of the first two rows and the last two columns

25. **Setting multiple columns**
And set the entire range of cells to the same value.

26. **Let's practice!**
Let's practice accessing data in DataFrames!