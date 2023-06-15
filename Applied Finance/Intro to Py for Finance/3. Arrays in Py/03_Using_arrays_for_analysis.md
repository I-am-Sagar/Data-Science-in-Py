1. **Using Arrays for Analyses**
In the last lesson, you used indexing to slice elements from multidimensional arrays. A powerful characteristic of NumPy arrays is that they can also be indexed with other arrays.

2. **Indexing Arrays**
Consider a 1-dimensional array, months_array. Now, let's create an "indexing array" that specifies specific indices, in this case 1, 3, and 5. You can now subset the months_array with this indexing array and store this solution as months_subset. In the months_array, indices 1, 3, and 5 correspond to months Feb Apr and Jun. And indeed, when we print out the result of months_subset, we see this result.

3. **More on indexing arrays**
What do you think would be the output of using an indexing array with negative indices like the one shown here? The output returned is the -1 indexed element, Jun, and then the -2 indexed element, or May.

4. **Boolean arrays**
Arrays can be comprised of numerics, strings or boolean values as shown here. A powerful characteristic of boolean arrays is that they can be used to manipulate other arrays. For example, consider the months_array and boolean_array arrays shown here. The boolean array would subset only the elements where the index is True. Thus, the output returned is Jan, Feb, and Mar.

5. **More on Boolean arrays**
Boolean arrays can also be created with conditional tests. In this example, we create a boolean array using a conditional test which identifies the elements in prices_array greater than 238. We can now use this boolean_array as an index to subset our prices_array.

6. **Let's practice!**
You can perform very powerful analyses combining boolean indexing and functions in numpy. Let's practice doing that!