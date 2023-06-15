1. **Dictionaries**
Now let's look at one of the most used data structures in Python, the dictionary.

2. **Lookup by index**
In the prerequisite course, you were introduced to lists and Numpy arrays. Both of these powerful data structures store data in an ordered fashion. This means that when you create a list, every item in the list has an index number describing where it is and how to access it. You can access an item by using its index with square brackets or determine it's index using its value.

3. **Lookup by key**
Dictionaries do not have the concept of an index, rather they store and lookup items using a key. Each item has a unique key, and with this key, you can access the item. When we say that a key is unique, we mean that it can only be used to represent one item in a dictionary.

4. **Representation**
Dictionaries in Python are represented as a series of key-value pairs separated by colons and enclosed in curly brackets. Here we have three key-value pairs, with key-1 associated with value-1, key-2 with value-2, and key-3 associated with value-3.

5. **Creating dictionaries**
We can create an empty dictionary by either using empty curly brackets or by using the dict() function.

6. **Creating dictionaries**
You can create a dictionary with initial values by expressing the keys and values in curly brackets during creation. Or as a list of key-value pairs, each contained in a sub-list. You can use either method, though the first is more common.

7. **Adding to dictionaries**
To add a new key-value pair to an existing dictionary, put the new value on the right of an assignment operator, and on the left, put the dictionary with the new key enclosed in square brackets. You can use the same syntax to update the value associated with an existing key. The ticker symbol for the oil company Exxon changed after its merger with Mobile, so here we indicate this with the old symbol.

8. **Accessing values**
To access values stored in a dictionary, enclose the key in square brackets after the dictionary, much as you would do with an index number when accessing items in a list. Here we use the key capital f to get the associated value, Ford.

9. **Accessing values**
If you try to access a key that is not mapped in the dictionary, an error will be thrown, and your program will exit. To avoid this, you could write code to ensure that the key is mapped in the dictionary before accessing it.

10. **Accessing values**
There is a simpler way though. Python dictionaries have a get method that protects against these errors. Invoke this method with a key as the argument, and it will return the key's value. If the key is missing, the special value none is returned. You can also supply a second argument, which will be returned instead of none if you request a missing key.

11. **Deleting from dictionaries**
There are times you will want to remove key-value pairs from a dictionary. In our example, we have a key for an outdated ticker symbol, XON. To remove a key-value pair, use the del function with the dictionary and bracketed key as the argument. See that after we do this, the unwanted key and its value are removed from the dictionary.

12. **Let's practice!**
You've learned how to create and manipulate Python dictionaries, now let's practice!