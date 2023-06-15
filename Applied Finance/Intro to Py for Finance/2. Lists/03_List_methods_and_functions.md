1. **Methods and functions**
2. **Methods vs. Functions**
We will now talk about methods. While all methods are functions in Python, not all functions are methods. There is a key difference between functions and methods. As we've seen, functions take objects as inputs or are "passed" an object. Methods, in contrast, act on objects. For example, the function type(), which tells us what data type a variable is, requires an input of an object like the list prices. Whereas the method sort() is "called" on a list named prices. Let's take a closer look at using methods spcific to lists.

3. **List Methods - sort**
To access methods of a list, you reference the list variable, followed by a period, followed by the name of the method. Suppose you want to sort the elements in prices in ascending order, you would type prices followed by a period, followed by the method name, that is sort, including the parentheses. There are many useful list methods, let's learn a few more.

4. **Adding to a list with append and extend**
You can add elements to a list using the append() method. The append() method adds a single element towards the end of a list. For example, let's append the string "April" to a list of months. To do this, you'll provide the string "April" to the list method append(). Using append() will always increase the length of the list by 1. If you would like to add multiple elements to a list, you can use the extend() method. Here we show how to add three elements to the list months. Unlike the append() method which increases the length of list by one, the extend() method increases the length by the number of elements that are provided to it.

5. **Useful list methods - index**
Let's learn about another list method called index(). index() returns the index of a specific element. Here are two lists, months and prices, which describe the month and consumer price index for that month. Let's use the index() method to find out the index of 'February'. Using this method identifies that February is at index 1. The corresponsing price for February can now be accessed using this index.

6. **More functions ...**
We can use list methods and functions to perform analysis in python. Let's introduce two more functions in Python: min() which returns the smallest element of a list and max() which returns the largest element in a list.

7. **Find the month with smallest CPI**
To identify the month with the smallest consumer price index, you'd first use the min() function on prices to identify the min_price. Next, you can use the index() method to identify the indexed location of the min_price. Using this indexed location on months, you can now identify the month with the smallest consumer price index, which turns out to be February.

8. **Let's practice!**
Now that you've learned about functions and methods, let's practice using them!

