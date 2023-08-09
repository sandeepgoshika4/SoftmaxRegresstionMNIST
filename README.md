# SoftmaxRegresstionMNIST
SoftmaxRegresstionMNIST

A logistic regression model is implemented in the provided code using manual computation using PyTorch for mathematical operations.

#Manual Logistic Regression Implementation:
In the manual implementation, a class named LogisticRegression1 is defined. Here's an overview of how it works:

* The class is initialized with the number of input features (num_features). It creates the model's weights (self.weights) and bias (self.bias) tensors, both initialized to zeros. These tensors are placed on the available device (CPU or GPU).
*  The forward method takes input data x and computes the linear combination of the input features with the model's weights, followed by applying the sigmoid function. The sigmoid function maps the linear combination to a probability value between 0 and 1, representing the predicted class probability.
*  The backward method computes the gradients of the loss with respect to the model's weights and bias. This involves computing the difference between the predicted probabilities and the actual target values, and then calculating the gradients using these differences and the input features.
*  The train method performs the training loop. It iteratively computes forward passes, backward passes, and updates the model's weights and bias using gradient descent. It also calculates and logs the negative log likelihood loss (logit cost) and the accuracy on the training set.
*  The predict_labels method uses the trained model to predict class labels based on a threshold of 0.5 on the predicted probabilities. The evaluate method computes the accuracy of the model's predictions on a given dataset.
*  The _sigmoid method implements the sigmoid function, and the _logit_cost method calculates the logit cost (negative log likelihood) for the given predictions and target labels.
*  The model's training progress is visualized using a plot of the negative log likelihood loss over epochs.
*  The manual implementation also computes and visualizes the decision boundary based on the learned model parameters.

# how the visualization of the 2D decision boundary works
* After training the model, you have learned weights (w) and bias (b) that define the decision boundary. These parameters are used to calculate the slope and intercept of the line that separates the classes.
* The slope of the decision boundary line is given by -w[0] / w[1], and the intercept is given by -b / w[1] (assuming a 2D feature space with two features). This is derived from the equation of a line: y = mx + b, where m is the slope and b is the intercept.
* Using the slope and intercept, you can compute the y values for two x values that represent the range of your data. These x and y values define the coordinates of two points on the decision boundary line. By plotting a line segment connecting these two points, you visualize the decision boundary in the feature space.


