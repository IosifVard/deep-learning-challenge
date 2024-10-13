## Written Report

1. Data Preprocessing:

- What variable(s) are the target(s) for your model?
IS_SUCCESSFULL is the target variable for the model

- What variable(s) are the features for your model?
The feature variables for the model are all the columns in the dataset except for IS_SUCCESSFULL and any ID or categorical columns that don't contribute to the prediction.

- What variable(s) should be removed from the input data because they are neither targets nor features?
EIN and NAME should be removed. EIN does not provide any predictive value. NAME is also irrelevant for the prediction and does not contribute to the model.

2. Compiling, Training, and Evaluating the Model:
- How many neurons, layers, and activation functions did you select for your neural network model, and why?
I used 3 layers and 1 output layer.
100 neurons used in the 1st layer. This is to capture complex patterns in the data at an early stage of processing.
50 neurons used in the 2nd layer. This reduces complexity slightly while maintaining a good capacity for learning.
30 neurons used in the 3rd layer. To prevent overfitting
I used relu (rectified linear unit) for 3 layers and sigmoid fort the output layer. relu is used due to its efficiency in learning non-linear relationships. Sigmoid is used for binary classification in the output layer.

- Were you able to achieve the target model performance?
The performance of the model was satisfactory but did not exceed expectations significantly. The accuracy was reasonable given the nature of the dataset, though there is room for improvement with additional tuning.

- What steps did you take in your attempts to increase model performance?
1st step: More neurons in the initial layer helped capture more complex relationships in the data (increased the number of neurons)
2nd step: Introduced dropout layers to help mitigate overfitting by randomly dropping units during training
3d step: By using 'ReduceLROnPlateau', the model's learning rate was adjusted based on performance, allowing the optimizer to fine-tune as training progressed.
4th step: Early stopping was implemented to halt training once the validation loss stopped improving, which helps prevent overfitting and saves computational resources.

 ## Summary: 
 
 - The deep learning model produced acceptable results for the charity donation success prediction problem. The model utilized three layers with 'relu' activation, dropout for regularization, and learning rate adjustment to enhance performance.
