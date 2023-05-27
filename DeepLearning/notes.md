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


