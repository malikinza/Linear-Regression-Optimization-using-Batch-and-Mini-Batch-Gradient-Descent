# Linear-Regression-using-Batch-and-Mini-Batch-Gradient-Descent

This project aims to optimize a linear regression model on a housing dataset, by finding parameters (lambda regulizer, epochs and learning rate) that result in the minimum validation error and batch time. 

I split the dataset into 80:20 train to test ratio. Then, I applied a closed-form/ direct solution over a range of lambda values to find the optimal lamdba regularizer that resulted in the minimum root mean squared validation error.

Using the optimal lambda regulizer of 8 and fixed learning rate of 0.01, I applied batch gradient descent, which is an iterative optimization algorithm, to determine the minimum number of epochs neededed to minimize the validation error. Note that an epoch is an iteration of the entire dataset.

Next, I applied mini-batch gradient descent to various batch sizes (subsets of the dataset) to find the best batch size based on fastest convergence (shortest batch time) and minimum validation error. A batch size of 202 produced the minimum error. Similarly, I sweeped over various learning rates and found 0.11 to result in the minimum error. 

Finally, I implemented an adaptive learning rate scheme where I started with a mini-batch gradient descent with a large learning rate and then decreased the learning rate as I approached the local minima. The learning rate was updated at each step based on epochs. 


Smaller learning rates require more training epochs given the smaller changes made to the weights at each step, whereas larger learning rates result in rapid changes and require fewer epochs. As expected, the batch time increased with increasing epochs. However, the validation error did not decrease much with increasing epochs beyond 350 epochs. 





