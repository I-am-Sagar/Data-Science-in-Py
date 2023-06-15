1. **Representing time with datetimes**
Most problems in finance relate to changes over time.

2. **Datetimes**
Whether you are trying to predict the future direction the market will take

3. **Datetimes**
or analyzing the historical Cuban trade deficit, having a way to represent time is an important requirement.

4. **Datetimes**
Python's Standard Library includes the datetime module which includes some useful time and date related functionality. To represent a specific time, you can use datetime objects. These objects have attributes representing the year, month, date, hour, second, microsecond, and timezone. In order to create a datetime object, you must at least provide the year, month, and date. Here we have created a datetime object for Black Monday, an important date in the market crash of 1987.

5. **Datetime now**
You will find that capturing the current time in your program will often come in handy. You may want to create a record of when you preformed a particular calculation or check how long a calculation took to run. datetime provides a dot-now function which returns a datetime representing the current time.

6. **Datetime from string**
You can create datetime objects from string (text) objects using the string-parse-time function. This function takes two arguments, first is the string to convert, the second a format string.

7. **Datetime from string**
The format string contains format codes that are prefixed with percentage characters. There are format codes for years, with or without the century. And for months, using names or numbers. For the day of the month,

8. **Datetime from string**
For the weekday as a name or a number, the hour as 12 or 24 hour clock, minutes as a number,

9. **Datetime from string**
and seconds, microseconds, and AM/PM, among others.

10. **Datetime from string**
Notice that some of the format codes are not intuitive and can be easily confused, percent lowercase m for month, and percent uppercase m for minute are often confused. It is a good idea to consult the documentation when creating format strings.

11. **Datetime from string**
Let's make some format strings that fit different date formats. First, let's make one for this date-time string, which represents the crash of 1837. First, we want to represent the year, including the century, this uses the format code %Y. Remember, the format code for the month as a number is %m, and the format code for the day of the month is %d. If we put these together in a string with dashes in between, we have a format string matching our date format.

12. **Datetime from string**
Let look at another example. This date string represents the beginning of the panic of 1901, which was prompted both by the assassination of President McKinley and a drought. This date string begins with the day of the week. The format code for this is %A. The code for the day of the month is, again, %d. The code for the month as a full name is %B, and the year without century is %y. So the format string for this date string is as shown.

13. **String from datetime**
You can also create strings from datetimes using the string-from-time function. You will find this method useful when outputting dates to reports or as part of any communication with clients. This method uses the same format strings as the string-parse-time function.

14. **String from datetime**
Here we make a datetime for the beginning of the Great Depression and convert it to a string using short names for the day of the week and month.

15. **Let's practice!**
You've seen different ways to make datetime object, now practice making them yourself!
