# Alphabet Soup Charity Report

## Overview of the Analysis

The analysis in this challenge was meant to test how well the created neural network model could identify which applicants for funding would be successful if they were to receive funding from the non-profit foundation, Alphabet Soup. The model was trained using information about past applicant organizations and data regarding whether or not the organization was successful after receiving funding. 

In order to build the machine learning model, the initial data set of past applicant organizations was split using the 'train_test_split' function into multiple subcategories in both the predictors (applicant organization information) and the variable (success after funding). These subcategories of data allow for the model to learn and be trained from one set of data, while also providing an additional set of data that the model is unfamiliar with to use for analysis of the model's efficacy in predicting the applicant organization's long-term success after receiving funding. 

## Results

* Data Preprocessing :
    * __What variable is the target for the model?:__ In this model, the target, or the variable that the model is meant to predict, is the success of the applicant organization after it receives funding from Alphabet Soup. 
    * __What variables are the features for your model?__ The features of this model include the applicant organization's affiliation, classification, use_case (category of organization), status, income amount, special considerations, and the amount being asked for from Alphabet Soup.
    * __What variables should be removed from the input data because they are neither targets nor features?__ The variables of EIN (Employer Identification Number) and the name of the organization were removed from the input data as they are neither targets nor features. 
    
* Compiling, Training, and Evaluating the Model :
    * __How many neurons, layers, and activation functions did you select for your neural network, and why?:__ The number of layers was determined to be 2, and the number of neurons is based primarily on the input. The number of neurons in each layer was determined by the number of neurons in the previous layer. The input layer is the largest, the hidden layers should be incrementally smaller, and the final layer, the output layer, should be the smallest. The most common activation function, reLU, was used in this instance. 
    * __Were you able to achieve the target model performance?__ The initial model had an accuracy of 0.7268 after training and testing. While the target performance of 0.75 was not achieved, the optimized model did increase in accuracy to 0.7281. 
    * __What steps did you take in your attempts to increase model performance?__ In order to optimize the model performance, the column 'ASK_AMT', which indicates the amount of money the organization was asking for from Alphabet Soup, was transformed from individual integers to ranges of numbers in given bins. Additionally, the number of neurons in each layer was adjusted to be incrementally smaller than the last. There were 47 input features, so hidden layer 1 was assigned 35 neurons and hidden layer 2 was assigned 10 neurons. The number of epochs was also reduced to 50. Other attempts to make the model more accurate, which resulted in decreased model performance, included changing the activation functions of each layer, adding an additional layer, dropping the 'STATUS' and 'SPECIAL_CONSIDERATIONS' columns, selecting a different 'random_state' in the splitting of data, and changing the size/values of the bins for the 'ASK_AMT' column. 

## Summary
Overall, the model can somewhat accurately determine the success of applicant organizations that receive funding from Alphabet Soup based on the applicant organization's given data. At this point, other models could be used, specifically the logistic regression model. A logistic regression model is a simple model, but can often predict a binary result, such as "successful" or "not successful" applicant organizations after funding. 
