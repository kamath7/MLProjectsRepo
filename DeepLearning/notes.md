### Gradient Descent

ELi5 tldr - Imagine you have a magical box that can answer questions for you. But first, you need to teach it by giving it examples and telling it the correct answers. For example, if you show it a picture of a cat, you want it to say "cat."

To make the magical box learn, we need to adjust some settings inside it, just like tuning a radio. These settings are called "parameters." We want to find the right parameters that make the box give correct answers most of the time.

But how do we know if the box is giving correct answers? We need a special tool called a "loss function." It tells us how wrong the box's answer is compared to the correct answer. We want this wrongness to be as small as possible.

Here's where gradient descent comes in. Imagine you are climbing down a hill. You want to find the steepest path that takes you to the bottom quickly. The steepest path is the direction where the ground goes down the most.

In the magical box, we imagine that there's a hill, and we want to go down that hill to find the best parameters. We look at how wrong the box's answers are (the loss), and we try to go in the direction where the loss decreases the most.

We take small steps in that direction and keep repeating the process. Each time we take a step, we check if the loss gets smaller. If it does, we're going in the right direction! We keep going until the loss doesn't get much smaller or until we reach the bottom of the hill.

So, gradient descent is like going down a hill to find the best settings for the magical box. By taking small steps in the right direction, we can make the box better at giving correct answers. This helps the box learn and become smarter over time.

Neural networks are like a big team of these magical boxes working together, each doing a different part of the job. They all learn together to get better and better at answering questions or recognizing things like cats or dogs.


Explaination 

Gradient descent is an optimization algorithm commonly used in training neural networks. It is used to iteratively update the parameters (weights and biases) of the network in order to minimize a loss function, which measures the difference between the predicted output of the network and the true output.

Here's how gradient descent works in the context of neural networks:

Initialization: The parameters of the neural network, including weights and biases, are initialized with small random values.

Forward Propagation: An input is fed into the network, and it undergoes a series of computations through the network's layers. Each layer applies a linear transformation (weighted sum) followed by a non-linear activation function. This process is known as forward propagation and produces a predicted output.

Loss Calculation: The predicted output is compared to the true output using a loss function. Common loss functions include mean squared error (MSE) for regression problems and categorical cross-entropy for classification problems. The loss function quantifies the discrepancy between the predicted and true outputs.

Backward Propagation (Backpropagation): The gradient of the loss function with respect to the parameters of the network is computed. This is done by applying the chain rule of calculus, starting from the output layer and working backward through the network. The gradients capture the sensitivity of the loss function to changes in the parameters.

Parameter Update: The gradients computed in the previous step are used to update the parameters of the network. The goal is to adjust the parameters in a way that minimizes the loss function. This is where gradient descent comes into play.

a. Learning Rate: Before updating the parameters, a learning rate is multiplied by the gradients. The learning rate determines the step size of the parameter update. It is a hyperparameter that needs to be carefully chosen, as a high learning rate can cause overshooting and slow convergence, while a low learning rate can lead to slow training.

b. Gradient Descent: The parameters are updated by subtracting the product of the learning rate and the gradients from their current values. This update is performed for each parameter in the network.

Iteration: Steps 2-5 are repeated for multiple iterations (epochs) or until a termination criterion is met. In each iteration, a new batch of input data is fed into the network, and the parameters are updated based on the gradients computed from that batch.

By repeating the steps of forward propagation, loss calculation, backward propagation, and parameter update, gradient descent gradually adjusts the parameters of the neural network to minimize the loss function. This process is typically performed on batches of data to improve computational efficiency, and it is known as mini-batch gradient descent. The size of the batch is another hyperparameter that needs to be determined.

It's worth noting that there are different variants of gradient descent, such as stochastic gradient descent (SGD), which updates the parameters after each individual data point, and more advanced techniques like Adam and RMSprop that adapt the learning rate during training to achieve faster convergence.


### Perceptrons and LTUs

Imagine you have a friend who is really good at recognizing different animals. You show your friend a picture, and they tell you what animal it is. How do they do it?

Well, they look at different parts of the animal, like its ears, eyes, and tail. They pay attention to these features to figure out what animal it might be. They combine all this information and make a guess.

A neural network works in a similar way. It is like having many friends, called "neurons," working together to solve a problem. Each neuron looks at different parts of the input and helps make a decision.

One of the simplest types of neurons is called a "perceptron." Imagine it as a little decision-maker. It takes in some inputs, like the features of an animal, and makes a decision based on them.

The perceptron works like this: It multiplies each input by a number, called a "weight," which determines how important that input is. Then, it adds up all these weighted inputs and checks if the total is above a certain threshold. If it is, the perceptron says "yes," otherwise it says "no."

For example, if the perceptron is trying to recognize cats, it might look at features like pointy ears and a long tail. If the weighted sum of these features is above the threshold, it says "yes, it's a cat!"

But what if we have more complex problems? That's where "LTUs" come in. LTU stands for "Linear Threshold Unit." It's a bit like a perceptron, but it can do more complex calculations.

An LTU works by taking in multiple inputs, just like a perceptron. But instead of just checking if the weighted sum is above a threshold, an LTU also applies a non-linear function to the sum. This function helps the LTU make more complex decisions.

With this extra flexibility, an LTU can recognize not only simple shapes like cats but also more complicated things, like letters or even faces.

In a neural network, you have layers of these LTUs. Each LTU in a layer helps make a decision based on different features. These layers are connected, and the outputs of one layer become inputs for the next layer. By combining the decisions from all the LTUs, the neural network can solve more complex problems, like recognizing different types of animals, objects, or even understanding spoken words.

So, perceptrons and LTUs are like little decision-makers in a neural network. They help process information and work together to solve problems. By combining their efforts, neural networks can learn to recognize and understand many different things.


### Backpropagation

Backpropagation is a fundamental algorithm used in deep learning to train neural networks. It is a mathematical method that allows the network to learn from labeled training data and adjust its weights and biases to minimize the difference between its predicted outputs and the desired outputs.

The backpropagation algorithm works in two main phases: the forward pass and the backward pass.

Forward Pass: In the forward pass, the input data is fed into the neural network, and the activations of each neuron in the network are computed layer by layer. The input data propagates through the network, and the outputs are generated. Each neuron applies a weighted sum of its inputs, followed by an activation function, to produce its output. This process continues until the output layer is reached, and the predicted output of the network is obtained.

Backward Pass: In the backward pass, the computed outputs are compared to the desired outputs using a loss function, which measures the discrepancy between them. The goal is to minimize this loss. The algorithm then calculates the gradients of the loss function with respect to the weights and biases of the network using a technique called the chain rule from calculus.

The gradients represent the sensitivity of the loss function to changes in the network's parameters. They indicate the direction and magnitude of the adjustments needed to minimize the loss. The gradients are propagated backward through the network, layer by layer, starting from the output layer. Each neuron receives the gradient from the neurons in the next layer and uses it to compute its own contribution to the overall gradient.

Once the gradients have been computed, an optimization algorithm, such as gradient descent, is used to update the weights and biases of the network. The optimization algorithm adjusts the parameters in the direction opposite to the computed gradients, aiming to minimize the loss function. This iterative process of forward pass, backward pass, and parameter update continues until the network converges to a state where the loss is minimized, and the network's predictions match the desired outputs more accurately.

Backpropagation is a powerful technique that enables deep neural networks to learn complex patterns and make accurate predictions. It allows the network to automatically adjust its internal representations by iteratively fine-tuning the weights and biases based on the discrepancies between predicted and desired outputs.

### Activation Function

In deep learning, an activation function is a mathematical function applied to the output of a neuron or a layer of neurons in a neural network. The purpose of an activation function is to introduce non-linearities into the network, allowing it to learn and model complex relationships between inputs and outputs.

Here are some key purposes of activation functions in deep learning:

Non-linearity: Activation functions introduce non-linear transformations to the input data. Neural networks without activation functions would only be able to represent linear relationships between inputs and outputs. By introducing non-linearities, activation functions enable neural networks to learn and approximate complex, non-linear functions, which are common in real-world data and tasks.

Learning Complex Patterns: The non-linear properties of activation functions allow neural networks to learn and represent complex patterns and relationships in the data. Deep learning models with multiple layers can stack non-linear transformations on top of each other, enabling them to learn hierarchical representations of the input data.

Gradient Propagation: During the backpropagation algorithm, gradients are computed and propagated backward through the network to update the weights. Activation functions play a crucial role in determining the gradients that flow through the network. They ensure that the gradients can be properly computed and propagated, allowing the network to learn effectively. Activation functions with well-defined derivatives and a suitable range of output values are essential for stable and efficient gradient propagation.

Output Range Limitation: Activation functions can restrict the output values of neurons within a certain range. For example, some activation functions, such as the sigmoid or tanh functions, map their inputs to a range between 0 and 1 or -1 and 1, respectively. This can be beneficial in certain scenarios, such as binary classification problems, where the outputs need to be interpreted as probabilities or bounded values.

Sparsity and Regularization: Certain activation functions, such as the rectified linear unit (ReLU), exhibit sparsity properties. They can lead to sparse activation patterns, where only a subset of neurons is activated while others remain inactive. This can help with regularization and prevent overfitting by promoting sparse representations in the network.

There are several commonly used activation functions in deep learning, including sigmoid, tanh, ReLU, Leaky ReLU, and softmax. Each activation function has its own characteristics and is suited for different types of tasks and network architectures.

Overall, activation functions are essential components in deep learning models, enabling the network to learn complex patterns, introduce non-linearities, and propagate gradients effectively during training.


### Tensor


In TensorFlow, a tensor is a fundamental data structure used to represent and manipulate data in a computational graph. It is similar to a mathematical concept of a multi-dimensional array or matrix, but with additional capabilities and functionalities.

Here's a simple explanation of tensors:

Imagine you have a collection of numbers. If you have only one number, that's just a scalar. If you arrange the numbers in a row or a column, it becomes a vector. Now, if you arrange those vectors into a table or a grid, it becomes a matrix. In TensorFlow, a tensor is an extension of these concepts to represent arrays of any number of dimensions.

Tensors can have different ranks or dimensions. For example:

A rank-0 tensor is a scalar, representing a single number.
A rank-1 tensor is a vector, representing a sequence of numbers.
A rank-2 tensor is a matrix, representing a table of numbers.
A rank-3 tensor represents a cube of numbers, and so on.
Tensors in TensorFlow are more than just containers for numerical values. They also carry additional information, such as their shape and data type. The shape of a tensor refers to the number of dimensions it has and the size of each dimension. For example, a tensor of shape (2, 3) is a 2-dimensional tensor with 2 rows and 3 columns.

TensorFlow provides a wide range of operations and functions to perform mathematical computations on tensors efficiently. These operations can include arithmetic operations, matrix multiplications, element-wise operations, and more. Tensors are at the core of TensorFlow's computational graph, allowing you to build and manipulate complex deep learning models.

In summary, a tensor in TensorFlow is a fundamental data structure used to represent and operate on multi-dimensional arrays of numbers. It enables efficient computation and manipulation of data within TensorFlow's computational graph framework.