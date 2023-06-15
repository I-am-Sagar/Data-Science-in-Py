1. **Two Dimensional Arrays**
So far we have worked with one dimensional arrays. However, arrays in NumPy can also be multidimensional.

2. **Two-dimensional arrays**
Often financial or quantitative data comes in the form of a table, with rows and columns. It's natural to represent this type of data in a 2D array. To create a 2D array in NumPy, you can use the same array() function you used earlier. But instead of providing a single list as the input, you pass in a list of two lists as the input as shown here. In this case, we've passed two lists, months and prices, to create a 2D array. Our final 2D array consists of 2 rows (representing our two lists) and 3 columns (the number of elements inside each list).

3. **Array Methods**
Just like lists, NumPy arrays have several methods associated with them. Two useful methods include shape and size. Shape tells you the dimensions of an array. For example, here you can see the shape of the cpi_array, is 2 rows and 3 columns. The method size can be used to return the number of elements in the entire array, which is 6 in this example.

4. **Array Functions**
In addition to methods, there are several numpy functions you can use on arrays. For example, you can use NumPy's mean() and std() functions to calculate the mean and standard deviation of numeric arrays as shown here. Recall that to use functions from numpy, you need to make sure that the function name precedes with the alias and a period.

5. **The `arange()` function**
Another useful numpy function is arange(). You can use arange() to create an array of continuous numbers as shown here. The function arange() creates a numeric array given a start, end, and an optional step argument. Thus, arange with inputs 1 and 13 would create an array consisting of numbers 1 through 12. Note that if you do not explicitly specify a step, the default is 1. If you want to create an array consisting of only odd numbers, you can use the same command with a step of 2.

6. **The `transpose()` function**
You can also easily switch rows and columns of a numpy array using the transpose() function. Suppose you have an array as shown here: the first row is the numeric representation of the month and the second row is the consumer price index. After transposing this array, you can easily see the price index next to the month.

7. **Array Indexing for 2D arrays**
Even with two dimensional arrays, you use indices to subset and slice elements. For multidimensional arrays, you must identify indices and which dimension they correspond to. For example, let's take a look at our cpi_array, with 2 rows and 3 columns. To subset an element in the second row (row index 1) and third column (column index 2), we would specify the corresponding indices in brackets seperated by a comma. Remembering that Python is zero-indexed, the first index represents the element in the first dimension or row and the second index represents the element in the second dimension or column. Thus, the row-index 1 and column-index 2 would return 238.91. Likewise you can use slicing to subset multiple elements. Recall that the colon indicates that we want to obtain all elements in a specified dimension. Here we use this notation to obtain all row elements and elements in the third column.

8. **Let's practice!**
Let's practice working more with arrays!

