# deep-learning-challenge

## report 

# data processing
What is the target variable for your model?
ANSWER: The target variable for the model is the "Is-Successful" column, which indicates the effectiveness of fund utilization.

What are the feature variables for your model?
ANSWER: The feature variables in this model include NAME, APPLICATION, TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, INCOME_AMT, SPECIAL_CONSIDERATIONS, STATUS, and ASK_AMT.

Which variables should be removed from the input data?
ANSWER: EIN (Employer Identification Number) has been excluded because its numeric nature could potentially mislead the model. SPECIAL_CONSIDERATIONS could also be dropped due to its infrequent occurrence, making quantification challenging. Additionally, STATUS can be removed as all rows contain the same value of 1.


# about the model 
How did you configure the neural network model in terms of neurons, layers, and activation functions, and why?
ANSWER: The model consists of three hidden layers with a substantial number of neurons to enhance accuracy beyond 75%. The number of epochs remained unchanged. Initially, the first activation function was 'relu,' but switching the 2nd and 3rd layers to 'sigmoid' along with the output layer improved accuracy.

Did you successfully achieve the target model performance?
ANSWER: Yes, the target model performance was achieved.

What strategies did you employ to enhance model performance?
ANSWER: To improve efficiency, we converted the NAME column into data points, which had the most significant impact. Additionally, adding a third layer and utilizing the "sigmoid" activation function for the 2nd and 3rd layers contributed to the performance enhancement.


#### Summary
In summary, achieving an accuracy rate above 75% allows us to correctly classify test data points with a 75% success rate. Moreover, an applicant has an 80% likelihood of success when meeting the following criteria:

The applicant's NAME appears more than 5 times (indicating multiple applications).
The APPLICATION type falls into one of these categories: T3, T4, T5, T6, T7, T8, T10, or T19.
The application has one of the following CLASSIFICATION values: C1000, C2000, C3000, C1200, or C2100.
For recommendation purposes, the Random Forest model is a suitable choice due to its effectiveness in handling classification problems, achieving an accuracy rate of 78%.