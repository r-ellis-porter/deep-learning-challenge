# Deep Learning Challenge Report

## Overview

The purpose of this project is to optimize a deep learning model to predict the success of organizations funded by Alphabet Soup. This involves preprocessing the dataset, compiling, training, and evaluating the model, and then optimizing it to achieve a target predictive accuracy of higher than 75%.

## Results

### Data Preprocessing
- **Target Variable:** The target variable for the model is IS_SUCCESSFUL, which indicates whether the funding provided was successful.
- **Feature Variables:** The feature variables for the model include columns like APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, and SPECIAL_CONSIDERATIONS.
- **Variables Removed:** The columns EIN and NAME were dropped as they were non-beneficial for the model.

### Compiling, Training, and Evaluating the Model
- **Neurons, Layers, and Activation Functions:** The neural network model consists of two hidden layers with 8 and 5 neurons, respectively. ReLU activation function is used for both hidden layers, and a sigmoid activation function is used for the output layer.
- **Target Model Performance:** The initial model achieved an accuracy of approximately 72.63%, which is below the target performance of 75%.
- **Optimization Steps:** To improve model performance, various optimization methods were attempted, including adjusting activation functions, adding dropout layers, and tuning hyperparameters using Keras Tuner. The best-performing model achieved an accuracy of approximately 79.72%.

## Summary

The overall results of the deep learning model indicate that it was able to achieve the target predictive accuracy after optimization. The optimization process involved adjusting model architecture, activation functions, and hyperparameters to enhance model performance. However, further optimizations could still be explored to potentially improve accuracy further.

## Recommendation

While the deep learning model performed reasonably well in predicting the success of funded organizations, an alternative approach using a different model could also be considered. For instance, a gradient boosting algorithm like XGBoost or LightGBM could be explored, as they often perform well in binary classification tasks and are capable of handling large datasets efficiently. Additionally, ensemble methods like Random Forest could be investigated for their ability to mitigate overfitting and improve generalization performance.
