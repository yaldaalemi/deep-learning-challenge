# Deep Learning Challenge Report

## Background

The purpose of this challenge is to develop a machine learning model that aids in identifying applicants with the highest chance of success in their ventures, specifically for funding. The model is trained on data from over 34,000 organizations that have received funding and creates a binary classifier to predict whether an applicant is likely to be successful or not.

## Results

### Data Preprocessing

- **Target Variable**:
  - The target variable for the model is the column "IS_SUCCESSFUL," which indicates whether the money was effectively used.

- **Features**:
  - Initially, all columns except "EIN" and "NAME" were considered as features.
  - For improved model performance, the following columns were further removed from the input data: "STATUS" and "SPECIAL_CONSIDERATIONS."

### Compiling, Training, and Evaluating the Model

- **Model Configuration**:
  - Initially, a neural network model with 2 hidden layers was used:
    - First hidden layer: 80 neurons
    - Second hidden layer: 30 neurons
  - Activation function: ReLU
  - The choice of neuron count was based on the input layer's size and to maintain model efficiency.

- **Model Performance**:
  - The target accuracy was not achieved, and the model had an accuracy of 0.7306.

- **Steps to Improve Model Performance**:
  - Added an additional hidden layer.
  - Adjusted neuron counts for hidden layers: 90, 45, and 30 for the first, second, and third layers, respectively.
  - Reduced the number of epochs from 100 to 47 to prevent overfitting.
  - Removed two columns from the feature set.
  - Despite these adjustments, the accuracy only slightly improved to 0.7319, which is a negligible improvement.

## Conclusion

The model development process involved various iterations to improve accuracy. However, the achieved accuracy of 0.7319 is still below the target. Further experimentation and feature engineering may be necessary to achieve the desired performance. The choice of neural network architecture and hyperparameters can significantly impact model outcomes, and fine-tuning these aspects should be considered in future iterations.

This report provides insights into the model development process for predicting funding success, and the journey to improving model accuracy continues.
