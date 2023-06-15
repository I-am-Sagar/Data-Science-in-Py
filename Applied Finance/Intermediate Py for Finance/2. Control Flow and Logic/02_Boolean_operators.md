1. **Boolean operators**
Now lets talk about Boolean operations.

2. **Boolean logic**
You may have studied Boolean logic in a math, or philosophy class. But even if you haven't, you've almost certainly used it intuitively. Boolean logic, also referred to as Boolean algebra, was first formalized by the mathematician George Boole in the 19th century.

3. **What are Boolean operations?**
Boolean logic consists of operations done between True or False values. There are three of these operations: AND, also known as logical conjunction. OR, known as logical disjunction. And NOT, known as logical negation.

4. **Object evaluation**
In Python all objects evaluate to True or False for the purpose of these operations. The objects which evaluate as False are the constants False and None. Zero in any numeric type, including integers and floats. Anything with a length of zero, including empty strings, lists, and dictionaries. The objects that evaluate to True include just about everything else.

5. **The AND operator**
The AND operator is represented in Python by the lowercase keyword 'and'. It compares two items, and if both are true, it evaluates to true. If either is false, it evaluates to false.

6. **The OR operator**
The OR operator is represented in Python by the lowercase keyword 'or'. It evaluates to true if either of the items is true. This includes the case where both items are true. It only evaluates to false when both items are false.

7. **Short circuit.**
Both the 'and' and 'or' operations are short-circuit operations. The means that Python will stop evaluating the items they compare as soon as the result of the operation is determined. For example, let's say we have two methods, is_current() and is_investment(), which both return true or false. If we use these methods as inputs to an AND operation, and the first method returns false, the second method will not be called. Similarly if we use them with the OR operator, the second method will only be evaluated if the first returns false.

8. **The NOT operator**
The NOT operator is represented by the lowercase keyword 'not'. It returns the Boolean opposite of an item directly following it. So not true returns false and not false returns true.

9. **Order of operations with NOT**
The NOT operator is lower in the order of operations than non-Boolean operators. For example, we have an equality operation comparing two Booleans which evaluates to false. If we put the NOT operator in front of this, it negates the result of the operation, not the first item.

10. **Object evaluation**
Because object evaluate as True or False, you can use them with Boolean operators. For example, we can use the AND operator with a string.

11. **Object evaluation**
the OR operator with a list. An empty one in this example, which evaluates to False.

12. **Object evaluation**
Or the NOT operator with a dictionary. The dictionary is empty, which evaluates to False, so with the NOT operator, it evaluates to True.

13. **Returning objects**
Remember that the AND and OR operators only evaluate as many items as necessary. Both of these operators return the last item that they evaluate. So for an AND operation with two items that evaluate to True,such as two non-empty strings, the second item is returned. If the first object evaluates to False,as in the case of an empty list, that object is returned.

14. **Returning objects.**
In the case of an OR operation, if the first object evaluates to True, such as the number 13, it is returned. If the first object does not evaluate to True, the second object is returned.

15. **Let's practice!**
Now that you understand Boolean operators, let's practice using them in finance related situations.