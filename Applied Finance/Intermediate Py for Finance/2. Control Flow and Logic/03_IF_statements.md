1. **If statements**
Now lets talk about controlling the execution of your code using 'if' statements.

2. **Printing sales only**
Imagine you are given a dictionary with data about a securities transaction with keys for amount, symbol, and transaction type. As you've seen, to print the transaction amount, you use the key to get the value from the dictionary. But what if you only want to print the amount if the transaction is a sale? This is where an 'if' statement comes in.

3. **Compound statements**
An 'if' statement is one of what are known as compound statements. These are statements where the value of an expression in a control statement, controls the executions of a group of statements.

4. **Control Statement**
The control statement for 'if' statements consists of the keyword 'if' followed by an expression which evaluates to True or False. This expression is followed by a colon, which indicates the end of the control statement. The expression can be anything that evaluates to True or False, including comparison operations, inclusion operations, Boolean operations, or even an object by itself.

5. **Code blocks**
The group of statements which are controlled by the 'if' statement will only execute if the expression evaluates to True. These statements can be grouped together, in what is called a code block, by indenting them a consistent amount relative to the control statement. Alternatively, the statements can be separated by semi-colons and placed on the same line as the control statement.

6. **Printing sales only**
For our transaction example, we can use an 'if' statement that compares the value for the 'type' key as an expression, and have the print statement as our controlled statement. In the case of this transaction, the type is 'BUY', so our expression will evaluate to False, and the print statement will not execute.

7. **Printing sales only.**
If we use a transaction with type of 'SELL' however, then the print statement is executed.

8. **Else**
In addition to controlling the execution of a code block using an 'if' statement, we can branch our code using the 'else' and 'elif' keywords. The 'else' keyword is used to define code which should execute in the case that the 'if' statement's expression is False. Here we print "I found x in y" if x is contained in y, and print "No x in y" if it is not.

9. **Elif**
The 'elif' keyword lets you define an if statement that is only evaluated if the initial 'if' statement is False. 'elif' is followed by an expression in the same manner as in an 'if' statement. Here if x equals y, we print 'equals', if it is not, then we check if it is less than y.

10. **Elif**
You can stack multiple 'elif' statements to test for multiple conditions. In this example we print different messages in the cases where x is equal, less than, or greater than y; and if none of those are true, test if x is zero. We can also add an 'else' at the end to catch situations that none of the conditions are met.

11. **Else with elif**
Here we have added a final message in case x doesn't fit any of the conditions. As you can see, you can branch the logic in your code using 'if', 'else', and 'elif' statements.

12. **Let's practice!**
Let's practice branching code using if statements.