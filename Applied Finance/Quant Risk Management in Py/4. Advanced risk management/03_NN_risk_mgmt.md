1. **Neural network risk management**
Real-time portfolio adjustment is part of the risk management problem. We'll examine one cutting-edge technology, neural networks, currently used to perform real-time updating.

2. **Real-time portfolio updating**
Until now our risk management workflow has defined and estimated risk measures, and performed portfolio optimization. Modern portfolio managers want to adjust portfolio holdings as quickly as possible in response to market information. Unfortunately, performing portfolio optimization can be computationally very costly. A solution is to create a function taking current asset prices as input, and returning a set of portfolio weights for each asset. This only requires an evaluation of a function on real-time asset data, and the function can be updated every so often.

3. **Neural networks**
A neural network is a function: it takes an input (such as asset prices) and returns an output (such as portfolio weights). It's called a neural network because it contains interconnected processing nodes known as 'neurons', loosely resembling the connections between neurons in the brain. Neural networks have been around since the 1940s, but they have enjoyed a resurgence of development since the early 2000s. They are used to solve problems with large datasets, such as image recognition, financial analysis, and search engine performance. Very large neural networks make up "Deep Learning" and are a part of the Machine Learning discipline. In 2015, Google released Tensorflow, an open-source environment, initially in Python, for performing Deep Learning.

4. **Neural network structure**
For our purposes, a neural network is a function with three properties, called "layers": an input "layer", which takes the input or 'independent variables',

5. **Neural network structure**
one or more "hidden" layers, and

6. **Neural network structure**
an output layer, representing the output or dependent variables. These layers are "trained" to learn about the relationship between the input and the output, much like a regression.

7. **Neural network structure**
The idea is to take an input, such as historical asset prices, and feed it to the input layer.

8. **Neural network structure**
The input layer passes on this data to one or more hidden layers, updating internal parameters (also called "weights") to tease out patterns in the data.

9. **Neural network structure**
The hidden layer then passes on these patterns to the output layer.

10. **Neural network structure**
After further processing, the result is an output, such as our portfolio weights.

11. **Using neural networks for portfolio optimization**
We can assess how well the neural network did in creating its output by comparing it to pre-existing 'best' weights. These weights are found from portfolio optimization on historical data. The goal is to make the difference between the output and the historical "best" weights as small as possible. This is called "training" the network. Once the network has been trained, its internal weights are fixed and it can be used. When new asset prices are fed to the network as input, the output is the predicted best portfolio weights. Thus, the neural network automatically performs portfolio optimization, making it a very powerful tool for risk management.

12. **Creating neural networks in Python**
In Python we'll use a library called "Keras" to access neural networks built in Tensorflow. This hides a lot of the lower-level programming needed, allowing us to focus on portfolio optimization. There are many parameters that we won't describe in this section, but you can visit the "Introduction to Deep Learning with Keras" course in DataCamp if you're interested! To use Keras, we first need to import the kind of neural network--this is a 'Sequential' network going from input-to-hidden-to-output layers. Then we need to import the connections between layers (the arrows we saw previously). We'll connect all neurons together using 'Dense' layers. Next we'll define our neural network 'model' and create our hidden and output layers, using the `add()' method. Notice how the input layer is specified with the 'input_dim' keyword, which in our case covers the four assets in our investment bank portfolio. And since we also need four output weights, there are four "neurons" in the last output layer. Believe it or not, that's all we need to specify a neural network! Now we need to train it on our data.

13. **Training the network in Python**
We've put asset prices into the 'training_input' matrix and portfolio weights into the 'training_output' vector. These are used to train the network. The model is first compiled to specify the error minimization function and how optimization is performed. Then we "fit" the network to the data, which carries out the minimization. The number of iterations to fit the data is given with the 'epochs' keyword--generally more is better.

14. **Risk management in Python**
To use the network we can give it 'new_asset_prices' it has never seen before! The network evaluates the new asset prices using the `predict()' method, and returns a set of portfolio weights. Over time, of course, new asset prices will accumulate, and they provide valuable information. Re-training the network every so often on new data, and backtesting it on old data, is part of the neural network workflow.

15. **Let's practice!**
You're now in possession of one of the most important tools in data science, machine learning. Apply what you've learned to the global financial crisis!

