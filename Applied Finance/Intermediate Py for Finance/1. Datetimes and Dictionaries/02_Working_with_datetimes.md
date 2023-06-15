1. **Working with datetimes**
Now that you know how to create datetimes using different methods let us look at some things you can do with them.

2. **Datetime attributes**
datetime objects have quite a few attributes. For example, you can access numerical values for the year, month, day, minute, second.

3. **Comparing datetimes**
You can compare datetimes to each other based on the times that they represent. Python supplies operators for comparing objects. We will be going into more depth on these comparison operators in Chapter 2, but here are the operators for equals, less than, and greater than.

4. **Comparing datetimes**
Here are two datetimes related to international market downturns from 1997, when an investment crisis in East Asia rippled around the world causing an international mini-crash. We can use our comparison operators to see which event came first. First we ask, was the Asian crisis greater(later) than the mini crash, using the greater than operator to ask this. Then we ask was the Asian crisis less than (before) the mini crisis, using the less than operator. The world mini-crash came later and hence is treated as greater.

5. **Comparing datetimes**
If we create another datetime object for the same date as the beginning of the mini crash, we see that it compares as being equal to the first. So it is the value of the time that the datetime represents that is used for comparison.

6. **Difference between datetimes**
So now you know how to compare datetimes to see which represents a more recent time, but what if you want to understand how much time passed between two datetimes? In Python, when we subtract one datetime from another, the object returned is a timedelta, which represents the difference between two times. Timedelta objects have attributes for weeks, days, seconds, and microseconds.

7. **Difference between datetimes**
If we take a datetime representing the world mini-crash of 1997 and subtract one representing the Asian downturn, the returned object, which we have here named delta, is a timedelta. We can check its type and see this. We can also access the difference between the two datetimes by accessing its day's attribute.

8. **Creating relative datetimes**
What if you want to create a datetime relative to an existing datetime. For example, you have a datetime named dt, which represents January 14th, 2019. You wish to construct a new datetime, which is one week earlier. You could use the attributes of the first datetime to calculate a new one like this. But this method is not recommended. It does not work when the number of days crosses into the next month or year. If we subtract more days than the date, this would result in a negative date and so we get an error.

9. **Creating relative datetimes**
Instead of trying to manage the boundaries between months and years yourself, you should use timedeltas to create relative datetimes. Remember that a timedelta object was returned when we subtracted one datetime from another,so you can create your own timedelta, and use it as an offset to create a relative datetime.

10. **Creating relative datetimes**
To do this, import timedelta from the datetime module and create a timedelta object for the desired offset. You can specify the timedelta in weeks, days, hours, minutes, seconds, or microseconds. Then subtract the timedelta from your start datetime to get the new offset one.

11. **Creating relative datetimes**
timedelta will manage crossing temporal boundaries for you. Here we start with the datetime for January 14, 2019, and subtract a timedelta of 16 days. That brings us back to the previous year and month. The resulting datetime has the correct adjusted year, 2018, and month, December, thanks to the to timedelta's understanding of the boundaries. This is very powerful when you need to calculate re-occurring dates, for weekly financial reports, or when you want to look back at a specific amount of time when trying to understand the causation of market events.

12. **Let's practice!**
Now let's practice working with datetimes.