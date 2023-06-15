1. **Lists in Lists**
A list can contain multiple data types and can be made up of strings, integers or floats, or some combination of strings and numbers.

2. **Lists in Lists**
Additionally, a list can contain other lists, like in this example. We call this a nested list. Here we have a list cpi that describes information about the consumer price index. It is comprised of 2 lists describing the month and the corresponding price index.

3. **Subsetting Nested Lists**
You may recall how to subset a simple list, where each element can be referred to by zero-based indexing. The element found at index one from the simple list months is "Feb" standing for February. How does indexing in a nested list work? If we subset the element at index 1 of a nested list, such as cpi, the result is a list. Thus, the command cpi bracket 1 would return the list at index one that contains consumer prices.

4. **More on Subsetting Nested Lists**
We know that we can subset a list out of nested list using indexing. We can ALSO use indexing to subset elements from EACH OF THESE NESTED lists. Let's take a look at an example here. First, recall from the last slide that using the index 1 returns the consumer price index list. Next, we can use another set of square brackets with an index to subset a specific element from that list. In this example, we'll use the index 0 to subset the first element of our nested list, which is $238.11.

5. **Let's practice!**
Let's practice working with nested lists in the next set of exercises!