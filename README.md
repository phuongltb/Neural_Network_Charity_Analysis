# Neural_Network_Charity_Analysis
Create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

## Overview of the project
This project consists of the following:
  - Preprocessing Data for a Neural Network Model
  - Compile, Train, and Evaluate the Model
  - Optimize the Model
  - A Written Report on the Neural Network Model (README.md)
  
## Results:
  - Data Preprocessing: 
    * IS_SUCCESSFUL variable is considered the target for the model
    * The features for the model are APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, and ASK_AMT

        ![image](https://user-images.githubusercontent.com/110554264/209979703-c86e0516-25ef-4003-a3e4-638cead6f3e8.png)

    * EIN and NAME are neither targets nor features and should be removed from the input data

        ![image](https://user-images.githubusercontent.com/110554264/209979630-5b2f414e-8413-4336-9ddf-ba13049959c1.png)

        ![image](https://user-images.githubusercontent.com/110554264/209976203-a7874aea-e8b6-499e-a278-22f90e60d2ba.png)


  - Compiling, Training, and Evaluating the Model
    * The neural network model using Tensorflow Keras contains 2 hidden layers, 14 neurons per layer, and use ReLu activation function.  The output layer uses activation function Sigmoid. ReLU activation function was used to enable nonlinear relationships and for the classification output, sigmoid activation function was used to produce a probability output. The structure, the loss and accuracy of the model are shown as the images below:

      ![image](https://user-images.githubusercontent.com/110554264/209979983-faab36b5-363e-4a73-bd8d-a9395ce1bdba.png)

      ![image](https://user-images.githubusercontent.com/110554264/209976562-bd96d0fb-3988-4c00-99c8-e8cb7c833f59.png)

      ![image](https://user-images.githubusercontent.com/110554264/209976779-bef46fd7-ee0e-4cae-830e-3275ee37ca41.png)

    * The target model performance of 75% was not able to achieve. The predictive accuracy for this model was 72.46%

      ![image](https://user-images.githubusercontent.com/110554264/209980235-da85e259-4b53-49cd-a7d2-e71d82a893d9.png)

    * Three attempts were made to increase model performance using the following techniques:
      + Attemp 1: Creating more bins for rare occurrences in column CLASSIFICATION and adding one more hidden layer. The predictive accuracy was increased to 72.66%

          ![image](https://user-images.githubusercontent.com/110554264/209980702-6d71c73b-5d18-4de2-b791-16cc37debf90.png)

      + Attempt 2: Reducing the number of epochs to the training regimen from 100 to 50. The predictive accuracy was 72.58% 

          ![image](https://user-images.githubusercontent.com/110554264/209980749-82ef4458-a6bc-4692-b4a9-8b41124be9b2.png)

      + Attempt 3: Adding more neurons to a hidden layer applying the a good rule of thumb. There are 43 input variables so there should be 129 (43*3) neurons in the hidden layer. The predictive accuracy was increased to %72.64

          ![image](https://user-images.githubusercontent.com/110554264/209980781-399ef6c0-6f57-4ad0-9ae0-2988a9cb8277.png)


## Summary
The initial deep learning model had a predictive accuracy of 72.46% which is lower than the target performance of over 75%. Some techniques were deployed to increase the performance, such as adding more neurons to a hidden layer by applying the good rule of thumb to have two to three times the amount of neurons in the hidden layer as the number of inputs, but the expected performance was not achieved. Other attempts, which are to create more bins for rare occurrences in column CLASSIFICATION and reduce the number of epochs to 50, were made; however, the predictive accuracy was not improved significantly. 

Since the input data is tabular data, I would recommend to use Random Forest model to solve this classification problem. Random Forest is fairly robust and this model predicts the classification based on consensus of the trained learners instead of evaluating data depending on the number of neurons and hidden layers defined as deep learning models. 

  
 



