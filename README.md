# Report on the Neural Network Model

## Overview of the analysis: 
The purpose here is to analyze a dataset from a nonprofit foundation called 'Alphabet Soup' that wants a tool that can help it select the applicants for funding with the best chance of success in their ventures.

## Data Preprocessing
Data Source
The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. 

Alphabet Soup’s business team has provided a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are several columns that capture metadata about each organization, such as:

EIN and NAME—Identification columns
APPLICATION_TYPE—Alphabet Soup application type
AFFILIATION—Affiliated sector of industry
CLASSIFICATION—Government organization classification
USE_CASE—Use case for funding
ORGANIZATION—Organization type
STATUS—Active status
INCOME_AMT—Income classification
SPECIAL_CONSIDERATIONS—Special considerations for application
ASK_AMT—Funding amount requested
IS_SUCCESSFUL—Was the money used effectively

Neural Network Models:
Two neural network models were created to predict the successful candidates. The first model was created by applying some optimization methods but it did not achieve the 75% accuracy. This lead to a second optimized model which was created by adjusting the optimization methods to try and achieve 75% or greater accuracy.

The following steps were taken to create each of the models:

## ORIGINAL MODEL:
These are the steps taken to create this neural network model:

Data Preprocessing:
The data was preprocessed by reviewing the available variables.

The target variable:
o IS_SUCCESSFUL

The feature variables:
o APPLICATION_TYPE
o AFFILIATION
o CLASSIFICATION
o USE_CASE
o ORGANIZATION
o STATUS
o INCOME_AMT
o SPECIAL_CONSIDERATIONS
o ASK_AMT

Removed variable:
One variable was removed from the input data as it is neither target nor feature:
o EIN

Preprocessing
• Binning
The data preprocessing also included creating bins for two specific variables by creating cutoff values for value counts of the underlying categories. A bin called Other was created to store the categories with a value count of less than the cutoff value.

Compiling, Training, and Evaluating the Model
Once the data was preprocessed, the model was compiled, trained and evaluated by defining the following details:

• Neuron Layers
There were two hidden layers and an output layer created in this model. The first hidden layer contained 80 neurons and the second layer had 30 neurons.

• Activation Functions
Relu activation function was used for the hidden layers, whereas Sigmoid activation function was used for the output layer.

• Parameters
The model was trained based on a total of 5,981 parameters.

• Epochs
The model was then fitted and trained by using 100 epochs.

• Model Performance
This model was evaluated to have an accuracy score of 72.71% which is below the target performance of 75%.

## OPTIMIZED MODEL:
In order to improve the accuracy of the original model, following steps were taken:

1.	Dropping lesser columns/ variables
2.	Creating bins for an additional variable
3.	Decreasing the number of values for the Other bin for one of the variables
4.	Adding one more hidden layer
5.	Changing the number of neurons in each hidden layer

These are the steps taken to create this neural network model:

In order to improve the accuracy of the original model, following steps were taken:

1.	Dropping lesser columns/ variables
2.	Creating bins for an additional variable
3.	Decreasing the number of values for the Other bin for one of the variables
4.	Adding one more hidden layer
5.	Changing the number of neurons in each hidden layer

Data Preprocessing:
The data was preprocessed by reviewing the available variables.

The target variable:
o IS_SUCCESSFUL

The Feature Variables:
o NAME
o APPLICATION_TYPE
o AFFILIATION
o CLASSIFICATION
o USE_CASE
o ORGANIZATION
o STATUS
o INCOME_AMT
o SPECIAL_CONSIDERATIONS
o ASK_AMT

The Removed Variables
One variable was removed from the input data as it is neither target nor feature:
o EIN

Preprocessing 
• Binning
The data preprocessing also included creating bins for three specific variables (as compared to two variables in the original data) by creating cutoff values for value counts of the underlying categories. A  bin called Other was created to store the categories with a value count of less than the cutoff value.

Compiling, Training, and Evaluating the Model:
After preprocessing the data, the model was compiled, trained and evaluated by defining the following details:

• Neuron Layers
There were three hidden layers (as compared to two in the original model) and an output layer created in this model. The first hidden layer contained 30 neurons, the second layer had 27 and the third layer had 21 neurons.

• Activation Functions
Relu activation function was used for the hidden layers, whereas Sigmoid activation function was used for the output layer.

• Parameters
The model was trained based on a total of 9,487 parameters.

• Epochs
The model was then fitted and trained by using 100 epochs.

• Model Performance
This optimized model was evaluated to have an accuracy score of 77.87% which is above the target performance of 75% and 5% higher than the original model.


# Summary:
After evaluating both the models, my recommendation is to use the optimized model to help predict the successful candidates for charity funding at Alphabet Soup. 

A few things that I found were, the optimized model yielded an overall better accuracy score of 77.47% compared to the original model at 72.42% and it was also met the target accuracy of 75% or higher. 
Along with this, this model uses one additional feature variable from the input dataset to predict the target variable. It also includes bins created for an additional variable as well as additional bins created for one of the variables compared to the original model. Adding the bins seemed to have improved the outcome of this model.

An additional hidden layer was added in the optimized model to make it a total of three hidden layers. It does, however, has lesser number of neurons for the first two hidden layers. This implies that although the overall number of neurons were lesser in the optimized model, however, the increased number of layers ended up increasing the number of trained parameters which eventually affected the accuracy of this model in a positive manner.

The recommended model in this case is definitely the second optimized model as it was more accurately able to predict the successful candidates for charity funding based on the change in optimization methods.
