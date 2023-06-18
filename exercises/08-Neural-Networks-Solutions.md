# 08 - Neural Networks

1. Architecture of a perceptron:
   - Input Layer
	   - input neurons
   - Output layer
	   - output neurons
   - Biased neuron

2. How does a perceptron work?
   Perceptron works based on Hebbian Learning, hence "cells that fire together, wire together". Each neuron has a weight to multiply the the input and the sum of all combinations is compared agains the **threshold logic unit (TLU)**.
   Classification takes place depending on the output value being bigger or smaller than the TLU.

3. Fully connected layer: tells that every neuron in a layer are connected to the every neuron in the previous layer.

4. What kind of problems are solvable with single layer perceptrons: binary classification problems

5. What is a multilayer perceptron (feed forward network) ?
   The signal flows in one direction (from input layers to output layers)
   
6. Backpropagation: uses gradient descent to minimize the neural networks error by tweaking the weights of each parameter according to the calculated error (mean squared error, absolute mean error or Huber loss [combination of both])

7. Why do we need activation function with nonzero derivate?
   Chaining of neurons is has a linear nature. If we stick to the linear nature we won't be able to tackle complex problems. Activation function introduces nonlinearity between layers.

8. Default activation function: sigmoid / tanh / ReLU

9. How many output neurons are needed for regression tasks?
   For single value predictions -> single output
   Multivariate regression -> 1 output per output dimension
   
10. What type of activation functions should you use for the last layer in a regression task? Describe different situations and corresponding activation functions.
    - In general no activation function for the output layer is preferred, so they can output any range of values.
    - If we want to guarantee that the output is + -> ReLU
    - If we want to guarantee that the output is within a certain range ->
	    - logistic function -> scale labels 0 to 1
	    - hyperbolic tangent -> scale labels -1 to 1

11. What type of activation functions should be used for the last layer in a classification task? Describe different situations and the corresponding activation functions.
    -  Binary classification -> logistic activation function, output is [0, 1]
    -  Multilabel binary classification -> logistic activation function, to each output neuron
    - Multiclass classification -> softmax for whole output layer, all probabilities add up to 1

12. How is loss function defined for classification?
    Cross-entropy is generally a good choice.