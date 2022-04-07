# Neural_Network_Charity_Analysis

## Overview of the analysis

The purpose of this analysis was to create a binary classifier that predicts whether applicant organizations will be successful if funded by Alphabet Soup. We used neural networks and deep learning to determine which class (successful or unsuccessful) an applicant fell into.

## Results

- Data Preprocessing
    - The IS_SUCCESSFUL variable is the target for this model. It is successful if it is a 1 and unsuccessful if it is a 0.
    - The features of this model are the categorical variables: APPLICATION_TYPE,  AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, INCOME_AMT, SPECIAL_CONSIDERATIONS.
    - EIN and NAME are neither targets nor features, thus they were dropped from the input data before the model was created.

- Compiling, Training, and Evaluating the Model
    - I tried multiple attempts at different levels and kinds of neurons, layers, and activation functions. In the original attempt, I used 80 nodes in hidden layer 1 and 30 nodes in hidden layer 2, both with ReLU activation functions and a Sigmoid output layer. With 100 epochs, the original model gave us 47.5% accuracy.
    - My next try, I was not sure where to start, so I did multiple changes to the model. I added a hidden layer, for a total of 3. I had 80 nodes in the first, 40 nodes in the second, and 20 nodes in the third. I kept the activations consistent, so all 3 were ReLU with a Sigmoid output layer. I also changed the number of epochs to 150. This proved more time consuming, but I had a higher accuracy in this model of 63.5%.
    - For my second attempt at optimizing, I decided to try dropping two columns that may not have had a strong effect on the data. I dropped USE_CASE and SPECIAL_CONSIDERATIONS. I changed the number of number of layers back to 2, but I left the nodes at 80 and 40, rather than going back to the 30 nodes in the second layer within the original model. I also changed the second layer to a Sigmoid activation to see what would happen. Finally, I reduced the epochs back to 100 because I felt that the extra 50 epochs weren't necessary. Unfortunately, this model's accuracy decreased from the previous model and only came to 53.0%.
    - For my final attempt, I added back in the 2 columns I had dropped. This time, I attempted to change the number of unique values that were binned in both the APPLICATION_TYPE counts and the CLASSIFICATION counts. I kept 2 hidden layers, but changed the second hidden layer back to 30 nodes. I left the first at 80, as has been consistent throughout all of my modelling attempts. I also changed the activation type of the second hidden layer back to ReLU. I was excited to see the model reach 70.3% accuracy.
    - Unfortunately, I was not able to reach the 75% accuracy that was the target for this challenge.
    - I attempted to change different factors in each of the modelling attempts in order to reach the desired accuracy level. At first, I tried to make things more complex; however, I realized that the accuracy was not increasing, so I made it more basic by my final attempt and was rewarded with higher accuracy. 


## Summary

Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and explain your recommendation.