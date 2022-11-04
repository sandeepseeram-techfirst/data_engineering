In machine learning, data splitting is typically done to avoid overfitting. 
That is an instance where a machine learning model fits its training data too well and fails to reliably fit additional data.
The original data in a machine learning model is typically taken and split into three or four sets.


The flaw with evaluating a predictive model on training data is that it does not inform you on how
well the model has generalized to new unseen data. A model that is selected for its accuracy on the
training dataset rather than its accuracy on an unseen test dataset is very likely to have lower
accuracy on an unseen test dataset. The reason is that the model is not as generalized. It has
specialized to the structure in the training dataset. This is called overfitting.