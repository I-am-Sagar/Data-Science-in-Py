1. **Variable Data Types**
All variables in Python are typed - and I don't just mean on your keyboard! The type of a Python variable defines its properties and how it can be used.

2. **Python Data Types**
Here are four data types in Python. Strings are text enclosed in quotes. Integers are whole numbers without decimal points, like the number 40. Floats are real numbers with a decimal point. Finally, booleans in Python are logical values, either True or False.

3. **Variable Types**
Note that unlike other programming launguages such as C or C++, Python sets the data type of the variable based on the value that is assigned to it. The abbreviations for the data types we discussed are shown here.

4. **What data type is a variable: type()**
It is often important to know the data type of the variable you are dealing with. To do this, you can use the function type() followed by the variable inside parentheses. We will learn more about functions in a later chapter. For now, think of functions as commands that you use obtain specific results. In this case, we used the type() function to determine the data type of a variable, and the print() function to print the result. As you can see here, the data type of pe_ratio is integer.

5. **Booleans**
Let's take a closer look at the Boolean data type. The Boolean data type is often the result of a conditional test involving comparison or logical operators.

6. **Boolean Example**
In this example, a double equal sign tests whether two values are equal, and since they are equal, the result is True. If you check the type of the result, you will see that it is bool, short for boolean.

7. **Variable manipulations**
As mentioned earlier, it is important to understand the data types of variables because depending on the data type of variables, you can manipulate them differently. Let's take a look at how strings and integers behave with the multiplication operator. Here we assign an integer 5 to the variable x and multiply this variable by 3. The solution is 15, an integer. Now let's assign the string 'stock' to the variable y and multiply it by 3. What happened? The string 'stock' is repeated thrice. What happens when you try to use the addition operator? As expected, when you add 3 to the integer, you get a valid result, 8. However, when you try to add an integer 3 to the string, you get an error. You can not combine an integer with a string directly.

8. **Changing variable types**
If you wish to print combination of strings and ints/floats, you first need to convert the int/float to a string. You can do this using the str() function. As you can see here, the type() of pi is float. But after passing pi to the str() function, the type of new variable pi_string is str. You can now combine pi_string with any string using the addition operator, as we do here.

9. **Let's practice!**
Now that you've been introduced to variables, let's put this into practice.