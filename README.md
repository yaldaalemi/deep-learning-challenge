# Deep Learning Challenge Report 
# Background:
The purpose of this challenge is to make a machine learning model that helps the user to find the applicants for funding with the best chance of success in their ventures. The model was trained with data from more than 34000 organizations that have received funding  and creates a binary classifier to predict if the applicant is going to be successful or not. 

Results:

Data Preprocessing

What variable(s) are the target(s) for your model?

The column, "IS_SUCCESSFUL" which indicates if the money was used effectively or not is the target of the model. 

What variable(s) are the features for your model? What variable(s) should be removed from the input data because they are neither targets nor features?

Initially after removing the "EIN" & "NAME" columns I set all the other columns except the target, "IS_SUCCESSFUL" as the features, but then for enhancing the performance of the model I further removed columns 'STATUS' & 'SPECIAL_CONSIDERATIONS' as well. 

Compiling, Training, and Evaluating the Model

How many neurons, layers, and activation functions did you select for your neural network model, and why?
Were you able to achieve the target model performance?
What steps did you take in your attempts to increase model performance?

Initially I started with 2 hidden layers, the first one with 80 neurons and second one with 30 neurons. The reason that I chose 80 neurons for the first hidden layer was that the input layer had 43 neurons and 80 is almost twice that size and I chose 30 for the second hidden layer to avoid making the model too complex and slow. For the activation function Relu was used since it usually performs well for all of the models. The target accuracy was not achieved and the model had an accuracy of 0.7306122183799744. To improve the accuracy I added another hidden layer and set the number of neurons as 90, 45 and 30 for the first, second and the third hidden layers respectively. I also reduced the number of epochs from 100 to 47 to avoid over-training the data and removed two of the columns from the features as mentioned previously. Adding neurons, hidden layers, reducing the number of epochs and dropping the columns only increased the accuracy to 0.7318950295448303 which is just a negligible improvement. 

Below you can see the evaluation of the first and the second model in order:
![image](https://user-images.githubusercontent.com/117786659/229657056-2c4c1b62-35cc-4878-9882-24904db185e6.png)
![image](https://user-images.githubusercontent.com/117786659/229657110-0b0fcb97-2a43-45d0-bb68-672bb4474f41.png)

