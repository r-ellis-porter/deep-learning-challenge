# Deep Learning Challenge Report

## Overview

* The purpose of this project is to optimize a deep learning model to predict whether funding applicants will be successful in their ventures.

## Results

* Data Preprocessing
    
    * The target variable for these models is 'Is Successful' which is a binary classifier indicating whether a venture was successful.
    * The features used for the models are: Name, Application Type, Affiliation, Classification, Use Case, Organization, Status, Income Amount, Special Considerations,and Ask Amount.
    * EIM was removed from the dataset because it is neither a feature nor a target variable.

* Compiling, Training, and Evaluating the Models

    * The final neural network has an inital layer with 5 neurons, 8 hidden layers with a combined 70 total neurons. The model uses the sigmoid activation function and compiler, binary crossentropy loss function, and Adam optimizer. These parameters were chosen based on the dataset primarily consisting of binary data and the results of the hyperparameter tuning process
    * The model successfully achieved a rounded validation accuracy of 80% which is higher than the 75% target.
    * To increase performance of the model, I used kerastuner to optimize hyperparameters, here is the result with the highest accuracy:
        * 'activation': 'sigmoid'
        * 'first_units': 5
        * 'num_layers': 5
        * 'learning_rate': 0.001
        * 'units_0': 15
        * 'dropout_0': 0.1
        * 'units_1': 7
        * 'dropout_1': 0.1
        * 'units_2': 7
        * 'dropout_2': 0.4
        * 'units_3': 15
        * 'dropout_3': 0.2
        * 'units_4': 9
        * 'dropout_4': 0.2
        * 'units_5': 7
        * 'dropout_5': 0.0
        * 'units_6': 5
        * 'dropout_6': 0.2
        * 'units_7': 5
        * 'dropout_7': 0.4   

## Summary

    The tuned model achieved a validation accuracy of 80% which is higher than the 75% target and can be used to correctly classify whether a venture was successful within our range of acceptable error. Sigmoid activation function works well as a classifier for binary data and excels as a compiler, but I would experiment with tahn as the initial activation function and a mixture of relu and sigmoid in the hidden layers after isolated promising results in this project if higher accuracy was desired. The RandomForest model would also be a good alternative to the Sequential model as it works especially well with mixed categorical and numerical datasets like this one.
