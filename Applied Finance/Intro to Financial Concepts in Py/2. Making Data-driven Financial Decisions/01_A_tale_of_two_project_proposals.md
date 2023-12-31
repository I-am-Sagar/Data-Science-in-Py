1. **A tale of two project proposals**
In this chapter, you are the CEO of a New York City based transportation company. You will learn the basics of financial decision-making and project financing in order to figure out what types of projects would be the most beneficial for your firm to undertake.

2. **Common profitability analysis methods**
You will use 3 different methods for capital budgeting to analyze the relative profitability of potential projects. Each methodology has different pros and cons. In this video, you'll first learn about the two most commonly used methods: Net Present Value (NPV) and Internal Rate of Return (IRR).

3. **Net Present Value (NPV)**
Net present value, or NPV, is equal to the sum of all the discounted cash inflows and outflows of a given project, and is used to measure the profitability of a potential investment. Projects with larger cash flows and lower discount rates will have higher net present values. Conversely, increasing the discount rate or decreasing the cash flows will lead to a lower net present value. This is a relatively simple methodology, but it does not allow you to compare projects of different sizes or lengths, and it also requires the assumption of a discount rate. We covered calculating NPV using NumPy's dot npv function in the the last chapter. So let's move on to IRR.

4. **Internal Rate of Return (IRR)**
Internal Rate of Return, or IRR, is also a measure of the profitability of an investment, but results in a percentage change representing the investment rate of return of a project instead of the net present value.

5. **IRR in NumPy**
This allows you to compare projects of different sizes or lengths in relative terms despite the projects having entirely different cash flow values. The internal rate of return must be computed by solving for IRR in the NPV equation when set equal to 0, which is difficult to do by hand. Since the IRR calculation results in a percentage term, it also does not allow you to compare the total value of two projects.

6. **Let's practice!**
Time to put this into practice.