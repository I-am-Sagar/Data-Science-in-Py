1. **Creating a DataFrame**
Now let's talk about one of the most used data structures in data science and analysis, the Pandas DataFrame.

2. **Pandas**
Pandas is a third party library that you can import and use in your code. There is a convention of importing Pandas using the name-space 'pd'. This means that if you import Pandas this way, you can refer to it as 'pd' in your code. Here we print 'pd' and see that it is pointing to the pandas module.

3. **Pandas DataFrame**
The Pandas DataFrame is the most used element of the Pandas library. You can think of a DataFrame as being very like a spreadsheet or table. It consists of data labeled both with columns and an index. Here we have created an empty DataFrame.

4. **Pandas DataFrame**
The columns of a DataFrame run along the top and the index is the numbers on the left. You can create empty data frames and add data later, but the more common workflow to to pre-populate your DataFrame with data when you create it.

5. **From dict**
There are many way to create a pre-populated DataFrame. One option is to use a dictionary with each key representing a column name, and each key's value being a list of items to populate that column. We pass the dictionary to the DataFrame constructor using the 'data' parameter.

6. **From dict**
If we look at the resulting DataFrame, we see that the dictionary keys 'Bank Code', 'Account#', and 'Balance' are used as column labels.

7. **From list of dicts**
Another option is to use a list of dictionaries, with each dictionary representing a single row.

8. **From list of dicts**
The dictionary keys once again are used to designate the columns in the DataFrame.

9. **From list of lists**
We can also pass in the rows as a list of lists, with each list representing a row of values.

10. **From list of lists**
Notice that the columns have been given numerical names based on the position of the data in the lists.

11. **From list of lists with column names**
You can specify column names by using the column argument. It takes a list of column names.

12. **From list of lists with column names**
These are used as labels for the columns.

13. **Reading data**
In most cases you will create a DataFrame by reading data from an existing file or database. Pandas has methods for reading data from many different formats, including Excel, Json, Html, Python's pickle format, sql, and csv files. Lets look at reading csv files.

14. **CSV**
Csv stands for comma separated values. This is file format is widely used as an application independent way of storing tabular data. Generally these files consist of values, separated by commas. The top row can be used to specify column names, in which case it is referred to as a header.

15. **Reading a csv file**
To read a csv file into a DataFrame, simply supply the path of the file to the Pandas read_csv function.

16. **Reading a csv file**
The resulting DataFrame is populated with the data from the file. This simple way of reading data is one of the most widely used means of loading financial data for analysis and manipulation.

17. **Non-comma csv**
The csv extension is often used for files that use symbols other than commas as separators. Two common ones are tab-separated files and files using the bar symbol '|'. Here is an example of the bar-separated data.

18. **Non-comma csv**
To open these files, simply supply the symbol with the separator argument, 'sep' when calling read_csv.

19. **Non-comma csv**
And a DataFrame will be created just as it would with a comma-separated file.

20. **Let's practice!**
Now let's practice creating Pandas DataFrames!