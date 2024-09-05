# Deep Learning project
Sied H Mohamed
# Over view of the project
The objective of the current task is to analyses the success of charitable donations using deep-learning neural networks with the TensorFlow. I used python to generate the results by preprocessing the data, compile, train and evaluate the model, and optimize the model. 

# Data and Method.
I used the data [charity_data.csv ](https://github.com/SiedHM/Neural_Network_Charity_Analysis/blob/main/Resources/charity_data.csv) from GWU Bootcamp

Python 3.7.7, and Jupyter Notebook 6.0.3 is used to generate the results

# Results
## Data Preprocessing
Two columns[EIN and NAME ] that are not need for the machine learning estimation are removed. Unique values of all the remaining coulumns are checked and I found that the columns “APPLICATION_TYPE” and “CLASSIFICATION”    have more than 10 unique value and these two variables bucketed by creating an “other” category within these variables. 
List of categorical variables is created and encoded using one-hot encoder and the resulting categories are merged into original data frame by dropping the ordinal categorical columns. 
The data is slitted in to training and testing data
## Compiling, Training, and Evaluating the Model
A deep learning model with two hidden layers where the first hidden layer has 80 neurons and second had 30 neurons is built. The output layer is also included . For the two hidden layers, ReLU  activation frunction is used and sigmoid function is used for the output layer
In the model compilation, adam optimizer function and  binary_crossentropy the loss functions are used. 
These results in model accuracy of 73% which is under 75%. This is the baseline model and fig-1 below show the training accuracy and validation accuracy of the model.

![fig1](https://github.com/SiedHM/Neural_Network_Charity_Analysis/blob/main/Resources/accuracy_0.png)

To improve the accuracy, first, number of neurons of the hidden layer is increased, however, this does not improve the accuracy. Increasing number of neurons have risk of overfitting the model.  The accuracy level is still 73%.

![fig2](https://github.com/SiedHM/Neural_Network_Charity_Analysis/blob/main/Resources/accuracy.png)

Second, I add a third hidden layer, however, there is no improvement in the result.

![fig-3](https://github.com/SiedHM/Neural_Network_Charity_Analysis/blob/main/Resources/accuracy2.png)

Third, I changed the activation function of the hidden layers to tanh, however, no improvement in model accuracy.

![fig-4](https://github.com/SiedHM/Neural_Network_Charity_Analysis/blob/main/Resources/accuracy3.png)

# Summary
The above deep leaning results shows that the required 75% and above accuracy is not achieved, hence, I recommended to use the supervised machine learning models such as Gradient bosting model, Random Forest model, etc.





