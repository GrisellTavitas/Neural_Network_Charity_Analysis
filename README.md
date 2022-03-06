# Neural_Network_Charity_Analysis

## 1. Overview of the analysis.
As part of Beck's work and after all the analysis of the behaviour of more than 34,000 organizations that have received funding from Alphabet Soup; Beck has to predict which organizations are worth donating to and which are too high risk. 

## 2. Results: 

  ### Data Preprocessing
   **- What variable(s) are considered the target(s) for your model?**
       
The column "IS_SUCCESSFUL", refers to the affiermation if the money was effectively used or not. So, this would be our column target. 

   **What variable(s) are considered to be the features for your model?**
       
            - APPLICATION_TYPE
            - AFFILIATION
            - CLASSIFICATION
            - USE_CASE
            - ORGANIZATION
            - INCOME_AMT
            - SPECIAL_CONSIDERATIONS
            - ASK_AMT

   **- What variable(s) are neither targets nor features, and should be removed from the input data?**
        
The "EIN and NAME" wich are identification columns, need to be dropped, since they are not needed to perform the analysis. 

   ### Compiling, Training, and Evaluating the Model
   **- How many neurons, layers, and activation functions did you select for your neural network model, and why?**
        
At the first attempt of optimazing, we decided to reduce the number of unique values in the variable "ASK_AMT", additionally to the bucket that we already have done as well to the variables: "APPLICATION_TYPE" and "CLASSIFICATION". Which gave us a result of 65.30% of accuracy. 
        
![1st_attempt_0](https://user-images.githubusercontent.com/90433064/156916971-c4db193e-d613-4d43-ae06-0780904189f6.jpg)

![1st_attempt_1](https://user-images.githubusercontent.com/90433064/156916975-57b65255-6d68-4f00-b489-89e0d7e1591d.jpg)

![1st_attempt](https://user-images.githubusercontent.com/90433064/156916979-254d8fa0-e5c4-4a3a-9419-55192bac5432.jpg)


For the second attempt, we look to optimize the model by adding one more layer of 15 neurons, having as a result 68.66% if accuracy. 

![2nd_attempt_0](https://user-images.githubusercontent.com/90433064/156916986-761cfb79-0c8d-4f6f-a961-83c09f96e532.jpg)
    
![2nd_attempt](https://user-images.githubusercontent.com/90433064/156916996-507f95cf-adff-49f8-b860-cd0e2fbd1a7b.jpg)

And for the third attempt, we choose adding the number of epochs to 200 for the training regimen, which result on 68.02% of accuracy. 

![3rd_attempt_0](https://user-images.githubusercontent.com/90433064/156917003-0b52870f-4428-4e47-be00-66f8f85d1e60.jpg)

![3rd_attempt](https://user-images.githubusercontent.com/90433064/156917006-d77bc28e-af7f-4bac-b649-9a3de0770221.jpg)

   **- Were you able to achieve the target model performance?**
After three attempts we did not be able to achieve the target for the model performance. Since we know that as input data becomes more complex, neural networks will require more and more optimization tweaks to achieve their desired accuracy.

   **- What steps did you take to try and increase model performance?**
            - Creating more bins for rare occurrences in columns.
            - Adding more hidden layers.
            - Adding the number of epochs to the training regimen.

## 3. Summary.
After the three mentioned attempts, we noticed that the better performace occured when we added the hidden layer with 68.66% of accuracy, versus 52.82% of the original model; and we chose that option instead of adding neurons to avoid the risk to overfitting the model.
We could saw as well, that the performance went down when we added the number of epochs to the training regimen. 
After all these results and taking into account that we could not reach the performance expected for the predictions that the Foundation needs; I would suggest trying to analyze the data through a Supervised Machine Learning model, specifically through a logistic regression model, which could work well since we need to predict a binary dependent variable. 
