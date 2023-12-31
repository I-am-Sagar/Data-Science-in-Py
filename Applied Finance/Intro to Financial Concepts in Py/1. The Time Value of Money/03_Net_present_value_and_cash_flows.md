1. **Net present value and cash flows**
Most financial decisions rely on more than just a single number. Instead, they rely on comparing cash flows.

2. **Cash flows**
Cash flows are a series of gains or losses from an investment over time. For example, consider project 1, which requires an up-front initial investment of 100 dollars, generating a series of cash flows for the next four years. Project 2, on the other hand, has a more unusual structure, generating 100 dollars immediately and in year 1 as well, then requiring a net 100 dollar investment in Year 2, finally generating 200 dollars and 300 dollars in years 3 and 4 respectively. Which project is better? You might think of summing the cash flows, but you really can't do that. Each cash flow is generated at a different time. You will need to convert each cash flow to either present or future value before doing any comparisons.

3. **Discounting**
So you could do this the hard way, by calculating the present value of each and every payment and discount it by the proper period, sum all the present values together, as shown in this slide, and then repeat the same process over again for the second project.

4. **Arrays in NumPy**
Alternatively, you could simply use NumPy's dot npv function and calculate all of this at once, one line per project. But before we talk about the NPV function, let's do a quick recap on NumPy arrays. The dot array() function in NumPy takes a list of values, and turns this list into an array object. Using this array object, you can now perform operations on each element using a single operator. In this example, we create a numpy array object called array 1 by first passing in a list of the values 100, 200 and 300. You can then multiply each of the elements in the array by 2 simply by performing the multiplication on the object itself, outputting the values 200, 400, and 600.

5. **Net Present Value**
Now that you are able to put values into an array, you can pass an array of cash flows into the dot npv function, along with a discount rate. We'll get into the mathematics and the pros and cons of the NPV function in a later chapter, but for now, all you need to understand is that this is a heck of a lot easier than doing everything manually. By the way, project 2 had a higher net present value of 552 dollars compared to the 407 for project 1.

6. **Let's practice!**
Now it's time for you to do the heavy lifting!