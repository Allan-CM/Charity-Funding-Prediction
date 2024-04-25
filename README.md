# Charity Funding Prediction

## Overview
The objective of this project is to build a machine learning model to predict whether applicants will be successful if funded by a charity organization. We preprocess the data, optimize the model, and evaluate its performance.

## Preprocessing
### Data Cleaning
* Loaded the dataset from a CSV file.
* Dropped non-beneficial columns, 'EIN' and 'NAME'.
### Binning
* Binned 'APPLICATION_TYPE', 'CLASSIFICATION', and 'ASK_AMT' columns based on their frequency.
* Replaced application types with fewer than 500 occurrences, classifications with fewer than 1000 occurrences, and ask amounts with fewer than 1000 occurrences with 'Other'.
### Encoding Categorical Data
* Converted categorical data into numerical data using pd.get_dummies.
### Splitting Data
* Separated the data into features (X) and target (y) datasets.
* Split the data into training and testing sets using train_test_split.
### Scaling Data
* Standardized the features using StandardScaler.

## Model Optimization
### Optimization Attempt 1
#### Neural Network Model
* Created a sequential neural network with two hidden layers.
* The first hidden layer has 70 units with a 'relu' activation function.
* The second hidden layer has 25 units with a 'relu' activation function.
* The output layer has a single unit with a 'sigmoid' activation function.
#### Model Compilation
* Compiled the model using 'binary_crossentropy' as the loss function and 'adam' as the optimizer.
#### Model Training and Evaluation
* Trained the model for 100 epochs.
* Achieved an accuracy of approximately 72.49%.

### Optimization Attempt 2
#### Neural Network Model
* Modified the neural network architecture with increased units in the hidden layers.
* The first hidden layer has 90 units, and the second hidden layer has 45 units.
* The output layer remains the same.
#### Model Compilation, Training, and Evaluation
* Compiled the model using 'binary_crossentropy' as the loss function and 'adam' as the optimizer.
* Trained the model for 100 epochs.
* Achieved an accuracy of approximately 72.56%.

*** Optimization Attempt 3
#### Data Preprocessing
* Repeated data preprocessing steps with an additional column, 'ASK_AMT'.
#### Neural Network Model
* Modified the neural network architecture with increased units in the hidden layers and added a third hidden layer.
* The first hidden layer has 180 units, the second hidden layer has 90 units, and the third hidden layer has 45 units.
* Used 'LeakyReLU' activation for the first two hidden layers and 'relu' for the third.
* The output layer remains the same.
#### Model Compilation, Training, and Evaluation
* Compiled the model using 'binary_crossentropy' as the loss function and 'adam' as the optimizer.
* Trained the model for 200 epochs.
* Achieved an accuracy of approximately 72.40%.

## Conclusion
While various attempts were made to optimize the model, the accuracy remained relatively consistent around 72-73%. Further optimization and feature engineering might be necessary to improve the model's performance.


## Repository Organization
1. AlphabetSoupCharity --> Contains jupyter notebook script for the Neural networking model
2. AlphabetSoupCharity.h5 --> Model data in a HDF5 file 
3. AlphabetSoupCharity_Optimization --> Contains Jupyer notebook script with all optimization attemps
4. AlphabetSoupCharity_Optimization .h5 --> Model optimization data in a HDF5 file 
5. NN Model Report --> Neural Networking model analysis report
6. Resource Folder --> Contains Pictures in refence to the NN model report


