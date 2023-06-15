1. **Comparison operators**
In the world of finance, you will often need to compare data. Whether you need to detect which events happened first, or if you just want to know if a stock's closing price is higher than its opening price, making comparisons is a requirement.

2. **Python comparison operators**
Luckily, Python offers built-in comparison operators. These include operators for equality and order.

3. **Equality operator vs assignment**
The equality operator is used to test if two items have an equal value. It is represented by two equal signs, and should not be confused with a single equal sign, which is used to assign a value.

4. **Equality operator vs assignment**
So if you want to see if two numbers have the same value, use the double equals. And if you want to assign a value to a variable, use the single equals.

5. **Equality comparisons**
You can test the equality of any object or types in Python, including datetimes, numbers, dictionaries, and strings. The equality operator compares an item's value.

6. **Comparing datetimes**
So if we compare two datetimes, each representing the same date, the Equals operator returns True.

7. **Comparing dictionaries**
Dictionaries are equal if they have the same keys and values. And are not equal if the keys differ, or if any of the values differ. Here we change the closing price of dictionary d2, and it no longer evaluates as equal to dictionary d1.

8. **Comparing different types**
Some types, such as floating point numbers and integers can evaluate as equal. Here we compare a float and an int. But most types evaluate as not equal when compared with a different type. For example, a string and an integer will always evaluate as not being equal.

9. **Not equal operator**
The not equal operator is represented by a explanation point followed by a single equals sign. It returns True if the compared objects do not evaluate to being equal, and false otherwise.

10. **Order operators**
There are four operators used to determine order. That is they determine if an item's value is greater or less than another item's value. These operators are less than, less than or equal, greater than and greater than or equal.

11. **Less than operator**
The less than operator returns True if the item on the left has a lower value than the item on the right and False otherwise. For example, we can compare two integers, an integer and a float, or two strings. In this case all of them evaluate to True.

12. **Less than operator**
You can also compare objects, such as datetimes. In this example we compare two datetimes which evaluate to the same value, and so return False.

13. **Less than or equal operator**
The less than or equal operator returns True if the left item is less than or equal in value to the right one. Here we compare an small int against a larger one, returning True. A float which evaluates as being equal to an int, also returning True. And two strings, where the first is later in the alphabet, and hence evaluates as greater than the second and so returns False.

14. **Greater than operator**
The greater than operator evaluates to True if the item on the left is greater than that on the right, and False otherwise.

15. **Greater than or equal operator**
The greater than or equal operator functions similarly to the greater-than operator, except that it returns True if the left item is greater or equal to the right one.

16. **Order comparison across types**
One important difference when using order operators versus equality operators is how they handle comparing across types. While some comparisons across types will work, such as between a float and an int, most cross type order comparisons, such as between a string and an int, or a datetime and a float will cause an error.

17. **Let's practice!**
Now let's practice comparisons using operators.

