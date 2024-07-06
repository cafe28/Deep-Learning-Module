Report on the Neural Network Model

- Overview
This analysis aims to assess the performance of a neural network model created for the Alphabet Soup Charity organization. The model's primary goal is to predict the success of funding applications using various features. This report details the model's architecture, training process, and overall outcomes.

The business team at Alphabet Soup provided a CSV file containing data on over 34,000 organizations that have received funding over the years. This dataset includes numerous columns with metadata about each organization.
_______________________________________

- Data Preprocessing
Based on our existing dataframe application_df., target variable for this analysis was the 'IS_SUCCESSFUL' column, which defines the funding status.

The feature variables are all columns in the application_df except for the 'IS_SUCCESSFUL' column, which was excluded to define the feature set. The variable X comprises these columns and represents the features used by the model to predict the success of funding applications. Each column in X corresponds to a different feature, collectively forming the model's feature set.

Two asjustments were done in the orignal dataframe where both 'EIN' and 'NAME' columns were removed from the dataset because they were neither target variables nor relevant features for the model.

For the initial model in AlphabetSoupCharity.ipynb, rare values in the APPLICATION_TYPE and CLASSIFICATION columns were binned. Additionally, categorical values were encoded using pd.get_dummies().
_______________________________________

- Compiling, Training, and Evaluating the Model
Three attempts were made to achieve an accuracy level above 75%. The neural network consists of multiple hidden layers, all utilizing the Rectified Linear Unit (ReLU) activation function, and an output layer employing the sigmoid activation function.
In the first attempt, the neural network architecture consisted of a first hidden layer with 8 neurons and a second hidden layer with 5 neurons.

After training the initial model for 31 epochs, it produced the following evaluation results on the testing data:

Loss: 0.55
Accuracy: 0.72

Two attempts were made In AlphabetSoupCharity_Optimization 1 and 2 to optimize the model, in which:

1st Optimization Attempt: 
    The neural network architecture consisted of a first hidden layer with 80 neurons and a second hidden layer with 30 neurons. 
    After training for 120 epochs, it produced the following evaluation results on the testing data:
    
    Loss: 0.5613
    Accuracy: 0.7249

-----------

2nd Optimization Attempt: 
The neural network architecture consisted of a first hidden layer with 70 neurons and a second hidden layer with 51 neurons. 
    After training for 130 epochs, it produced the following evaluation results on the testing data:
    
    Loss: 0.5738
    Accuracy: 0.7265

_______________________________________


- Model Architecture:
    -Input Layer

    -Hidden Layers (Dense)
        -First hidden layer: 80 nodes, Rectified Linear Unit (ReLU) activation function
        -Subsequent hidden layers: X nodes, Rectified Linear Unit (ReLU) activation function

    -Output Layer (Dense)
        -1 node, Sigmoid activation function

- Activation Functions:

    - Hidden Layers: Rectified Linear Unit (ReLU)
    - Output Layer: Sigmoid

- Purpose
    - First Hidden Layer: Processes the input data with 8 nodes using the ReLU activation function.
    - Subsequent Hidden Layers: Further refine the features with X number of nodes using the ReLU activation function.
    - Output Layer: Produces a binary classification output (0 or 1) using the Sigmoid activation function, making it suitable for binary classification problems.
_______________________________________

Summary

Overall, the model's performance did not meet the criteria for implementation at the Alphabet Soup foundation. The model exhibited lower accuracy and a higher loss percentage, indicating significant room for improvement before it can be considered effective for practical deployment in predicting funding application success.












