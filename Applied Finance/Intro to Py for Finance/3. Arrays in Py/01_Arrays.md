1. **Arrays**
So far you've used methods and functions that are available by default in Python. It's now time to learn about the vast ecosystem of packages. A package is a collection of several Python scripts or modules introducing new functions, methods and datatypes.

2. **Installing packages**
Before you can use a package, you need to download it. You can use the command pip3 install package_name to install the relevant package. So, in order to install the numpy package which we will be using next, you can use pip3 install numpy. Note that you don't need to install packages in DataCamp courses as we have already installed them for you. You need to download a package only once, but you have to import it in your workspace everytime you wish to use the package.

3. **Importing packages**
To import a package use the import keyword followed by the package name. Thus to import the numpy package, type "import numpy". This command will load all the functionality of the numpy package into python for your use! In NumPy, we can create new datatypes, called arrays.

4. **NumPy and Arrays**
We first import numpy and then use the array() function to create an array. A couple of things to note: The array() function takes a list as its input and in order to access the array() function, you need to use numpy dot array to indicate that this function is from the numpy package. You can use the type() function as you did in the previous chapters to check the type of my_array, which is a numpy ndarray.

5. **Using an alias**
As you saw in the last slide, everytime you want to use a function from a package, you need to type the package_name and the function_name() which can get tedious. To make your life easier, you can use an alias to refer to the package by using the as keyword. For example, you can use the np alias for numpy by using the command import numpy as np. Now you can access all the functions from numpy using np dot function_name().

6. **Why use an array for financial analysis?**
You might be asking yourself how are arrays different from lists and why they are used? Arrays have several benefits over Python lists. They are more compact in how they store data, resulting in faster access in reading and writing items. This makes arrays more convenient and efficient for especially large datasets. Another reason to use arrays is that there are numerous array-associated functions within several Python packages that make trend modeling, statistics, and visualizations easier...all things that are important for finance.

7. **What's the difference?**
Arrays are different from lists because they can contain only a single data type. If you do create a numpy array with different data types as shown here, NumPy will automatically convert all the elements to the most compatible type. In this case, all the elements are converted to a string.

8. **Array operations**
Arrays are also different from lists in their operations. When you add two lists using the plus sign, the lists will be concatenated. However, when you add numpy arrays, the result is an element-wise sum of both the arrays.

9. **Array indexing**
Similar to Python lists, arrays can be indexed and sliced to subset elements. You can select a specific index element of an array using indexing notation or you can slice a range of elements using the slicing notation specifying a range of indices. Recall that the slicing notation in python is left inclusive and right exclusive.

10. **Array slicing with steps**
Similar to list slicing, you can specify a step size when slicing NumPy arrays. In this case, we specified a step of 2 to subset every other element in the array.

11. **Let's practice!**
It's now time to create your own NumPy arrays!
