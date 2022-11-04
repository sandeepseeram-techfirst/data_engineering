In machine learning, data splitting is typically done to avoid overfitting. 
That is an instance where a machine learning model fits its training data too well and fails to reliably fit additional data.
The original data in a machine learning model is typically taken and split into three or four sets.


The flaw with evaluating a predictive model on training data is that it does not inform you on how
well the model has generalized to new unseen data. A model that is selected for its accuracy on the
training dataset rather than its accuracy on an unseen test dataset is very likely to have lower
accuracy on an unseen test dataset. The reason is that the model is not as generalized. It has
specialized to the structure in the training dataset. This is called overfitting.


A neural network is a simple mechanism thats implemented with basic math. 
The only difference between the traditional programming model and a neural network is that you 
let the computer determine the parameters (weights and bias) by learning from training datasets.


Can we teach computers to learn like humans do, by combining the power of memorization and
generalization? It's not an easy question to answer, but by jointly training a wide linear model (for
memorization) alongside a deep neural network (for generalization), one can combine the strengths
of both to bring us one step closer. At Google, they call it Wide & Deep Learning. It's useful for generic
large-scale regression and classification problems with sparse inputs (categorical features with a
large number of possible feature values), such as recommender systems, search, and ranking
problems.


If model parameters are variables that get adjusted by training with existing data, your hyperparameters are the variables about the training process itself. 

For example, part of setting up a deep neural network is deciding how many "hidden" layers of nodes to use between the input layer and the output layer, as well as how many nodes each layer should use. These variables are not directly related to the training data at all. 

They are configuration variables. Another difference is that parameters change during a training job, while the hyperparameters are usually constant during a job.

Weights and biases are variables that get adjusted during the training process, so they are not hyperparameters.