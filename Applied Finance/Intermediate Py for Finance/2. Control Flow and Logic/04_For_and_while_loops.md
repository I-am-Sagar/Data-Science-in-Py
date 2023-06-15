1. **For and while loops**
This lesson is about 'for' and 'while' loops.

2. **Repeating a code block**
There will be situations where you will need to repeat an operation on multiple items. For example you might want to go through a list of transactions and look up the security symbol for each one, or maybe stop at the first one that involves Oracle securities.

3. **Loops.**
Python offers two compound statements for such operations, the 'for' loop and the 'while' loop. These statements let you run a code block multiple times.

4. **Statement components**
Just like the 'if' statement, these statements consist of two parts. A control statement and a code block. The control statement determines how many times the code block is executed.

5. **For loops**
Control statements for 'for' loops begin with the keyword 'for', which is followed by a variable, the keyword 'in' and a sequence. As in other control statements, it ends with a colon. The sequence can be any object that we can step through an item at time, such as a list, the keys of a dictionary or a string.

6. **List example**
The 'for' statement loops through the items in the sequence. For each iteration, it assigns the current item to the variable and executes the code block. In the case of a list, the variable is assigned to each item in the list. The variable can then be used in the code block, here we print its value.

7. **Dictionary example**
In the case of a dictionary, the variable is assigned to each key. Here we use the key in the block to print the dictionary's values.

8. **String example**
For a string, the variable is assigned to each character individually. In this example we print each letter separately.

9. **While control statements**
The control statement for a 'while' loop begins with the keyword 'while', which is followed by an expression and then a colon. As in an 'if' statement, the expression should evaluate to True or False. The 'while' loop will execute the code block repeatedly as long as the expression is True.

10. **While example**
Here we have a 'while' loop which executes a code block over and over again as long as the variable x is less than five. The block prints the value of x, and then increases it by one.

11. **Infinite loops**
It is important that your 'while' loop has a way to end. A common bug for beginning programmers is to use an expression that will always be true. Here we don't increment the variable, and so the test expression is always true. This will cause your program to loop infinitely.

12. **Skipping with continue**
The continue statement is used to skip a loop iteration. It is generally used in combination with an 'if' statement to skip iterations which meet some condition. In this example, we skip the iteration when the variable x is set to the number 2.

13. **Stopping with break.**
The 'break' statement is used to exit from a loop, without finishing iteration. It too is generally used in conjunction with an 'if' statement. In this example, we loop through a series of transactions, but stop our loop the first time we hit a transaction whose symbol is 'ORCL'. Notice that the control expression in this case is always True, so if we did not call 'break', this would be an infinite loop.

14. **Let's practice 'for' and 'while' loops!**
Let's practice looping with 'for' and 'while' loops!