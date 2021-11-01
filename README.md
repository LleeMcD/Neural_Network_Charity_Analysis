# Neural Network Charity Analysis
## Overview
The purpose of the analysis was to create a binary classifier that could predict whether applicants would be successfrul if funded by a charitable organization.
#### Data Preprocessing
The data set for this project consisted of a CSV file containing 12 columns and 34,299 rows. Four of the columns had a data type of integer (int64), the remaining columns were non-numerical (object). The data was prepped and normalized for use with the model.  
The target variable for the model was IS_SUCCESSUL, which was selected because it represents how often the donated money was used successfully by different recipients.
The features variables below were selected because they were most relevant to the target variable: 
- APPLICATION_TYPE 
- AFFILIATION
- CLASSIFICATION
- USE_CASE
- ORGANIZATION
- STATUS
- INCOME_AMT
- SPECIAL_CONSIDERATIONS
- ASK_AMT

Variables EIN and NAME were removed from the input data because they are not targets or features.
#### Compiling, Training, and Evaluating the Model
###### Neurons and Hidden Layers
The number of neurons comprising the input layer is equal to the number of features (columns) in the data. The following options were considered when selecting the number of hidden layers and associated number of nodes: 
- The number of hidden neurons should be  between the size of the input layer and the size of the output layer. 
- The number of hidden neurons should be 2/3 the size of the input layer, plus the size of the output layer. 
- The number of hidden neurons should be less than twice the size of the input layer. (StackExchange: https://stats.stackexchange.com/questions/181/how-to-choose-the-number-of-hidden-layers-and-nodes-in-a-feedforward-neural-netw

###### Activation Types
- The ReLU activation function was selected for the hidden layers because it is ideal for looking at positive nonlinear input data for classification or regression.
- The tanh function was selected for the optimization attempt with the hidden layers because it can be used for classification or regression, and it expands the range between -1 and 1.
- The Sigmoid activation function was selected for the output layer because the values are normalized to a probability between 0 and 1, which is ideal for binary classification.
###### Outcome
Target model performance could not be achieved.
The following steps were taken to increase model performance:
- The variable INCOME_AMT was dropped
- Additional neurons were added to the first hidden layer, they were increased from 80 to 120 nodes.
- An third hidden layer was added.
- The activation function for the first and second layers was changed to tanh.

Images of the code used for the optimation attempts follow the Summary section below.
#### Summary
An accuracy score of 75% or greater could not be achieved with this model, the highest score was 73% (0.7258). Linear regression, Random Forest or Support Vector Machine models may be more suited to this data set.

###### Optimization Attempts Code

![optimization_attempts](https://github.com/LleeMcD/Neural_Network_Charity_Analysis/blob/main/Resources/optimization_attempts.png)

###### Resources
- © 2020 - 2021 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.
- StackExchange: https://stats.stackexchange.com/questions/181/how-to-choose-the-number-of-hidden-layers-and-nodes-in-a-feedforward-neural-netw
