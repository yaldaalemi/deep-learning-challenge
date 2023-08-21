# Deep Learning Challenge Report

## Background

The objective of this challenge is to create a machine learning model that assists users in identifying applicants for funding with the highest likelihood of success in their ventures. The model was trained using data from over 34,000 organizations that have received funding, and it serves as a binary classifier to predict whether an applicant is likely to succeed or not.

## Results

### Data Preprocessing

**Target Variable**:
- The target variable for the model is the column "IS_SUCCESSFUL," which indicates the effective use of funds.

**Features**:
- Initially, after removing the "EIN" and "NAME" columns, all remaining columns, except the target "IS_SUCCESSFUL," were considered as features.
- For enhancing model performance, additional columns 'STATUS' and 'SPECIAL_CONSIDERATIONS' were removed from the input data.

### Compiling, Training, and Evaluating the Model

**Model Configuration**:
- The initial neural network model had 2 hidden layers:
  - First hidden layer: 80 neurons
  - Second hidden layer: 30 neurons
- ReLU was chosen as the activation function, which is known for its performance across various models.

**Model Performance**:
- The target accuracy was not achieved, resulting in a model accuracy of 0.7306.

**Steps to Improve Model Performance**:
- An additional hidden layer was added.
- The neuron counts for hidden layers were adjusted to 90, 45, and 30 for the first, second, and third layers, respectively.
- The number of epochs was reduced from 100 to 47 to prevent overfitting.
- Two columns were removed from the feature set, as previously mentioned.
- These adjustments led to a slight accuracy improvement, reaching 0.7319, which is a negligible increase.

### Model Evaluation

Below, you can see the evaluation of the first and second models in order:

![Model 1 Evaluation](https://user-images.githubusercontent.com/117786659/229657056-2c4c1b62-35cc-4878-9882-24904db185e6.png)

![Model 2 Evaluation](https://user-images.githubusercontent.com/117786659/229657110-0b0fcb97-2a43-45d0-bb68-672bb4474f41.png)
