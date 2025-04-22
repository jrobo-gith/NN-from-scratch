This project is: <b>INCOMPLETE</b><br>
This is part of the PORTFOLIO project - A list of projects designed to showcase various skills I love to learn. Projects include:

- [Regression techniques from scratch](https://github.com/jrobo-gith/Regression-techniques-from-scratch)
- [Building a neural network from scratch](https://github.com/jrobo-gith/NN-from-scratch)
- [Building CNN using Pytorch](https://github.com/jrobo-gith/MNIST-CNN)


# Building a Neural Network from scratch
Building neural networks with a package such as Pytorch is a streamlined way of building your first neural net. It (really usefully) wraps up the math used in these networks and makes it almost disappear. This workflow is optimised for two objectives: 1. to build your first neural network to get you intrigued without being slowed by the maths, and 2. for experts who already understand the math and would actually just like to work with the data. The middle ground, where one has built and tested neural networks using Pytorch, but are not absolutely confident about what goes on 'under the hood' is the problem I'm trying to fix. This problem needs fixing if I'm to understand how these processes can be adapted / optimised and eventually land a job in this field. Hence, this project is about addressing this problem by building a neural network from scratch, only using the numpy module. 

## 1. Where to begin?
A shallow neural network (NN) is composed of layers. An <i>input layer</i>, specifying a vector of inputs, a <i>hidden layer</i> where the magic happens, and an <i>output layer</i> releasing a vector of outputs. This shallow NN, given a large enough hidden layer, can approximate any function under the [universal approximation theorem](https://en.wikipedia.org/wiki/Universal_approximation_theorem), but in practice, needs so many nodes within this single hidden layer, that it becomes inefficient given some complex continuous function. An alternative is stacking these hidden layers together to form a deep neural network, able to achieve similar representations of continuous functions but using a lot fewer neurons (specific nodes in each layer). In image classification, it can also build up hierarchical representations, where the first layers look at the edges of the image, whilst the middle layers look at textures and shapes, and the latter layers detect objects.

## 2. Magic in the hidden layers

## 3. Steps to make a NN 

## 4. Translate this to code 

## Problems
One problem I ran into was the inputs to each layer were becoming increasingly large, eventually reaching $e^9$ near the end. This was because even though I had initialised my weights between 0 and 1, there was nothing stopping the inputs reaching incredibly large values due to the ReLU activation function not clamping any values.
I solve this using He initialisation, we initialise the weights according to a gaussian distribution with $\mu = 0$ and $\sigma = \sqrt{2/n}$ where $n$ is the number of input units, this works especially well for ReLU activation functions. This changed our code for the input weights, for example, to ```params = {"W_inputs": np.random.uniform(0, 1, size=(num_inputs, HL_structure[0]))}``` to ```params = {"W_inputs": np.random.normal(0, 2/num_inputs, size=(num_inputs, HL_structure[0]))}``` 


 

