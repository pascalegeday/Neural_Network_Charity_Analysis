# Neural Network Charity Analysis
## Overview
For this project, we are using Deep-Learning Neural Networks with the TensorFlow Library to predict whether applicants who apply for donations at the company, Alphabet Soup, will be successful if funded and also provide the overall results of the deep learning model used for this analysis.


## Resources
* Data Source: charity_data.csv
* Tools & Framework: Python, TensorFlow library, Scikit-learn Library

## Results

### Data Preprocessing for a Neural Network

- The variable `IS_SUCCESSFUL` contains binary data that decides whether the charity donation was succesful. As a result, this column is considered our target variable. 
- The variables, `APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT` are the features for our model.
- The variables `EIN` and `NAME` are categorical variables and are neither target nor features. For this reason, they have been removed from the input data.

### Compiling, Training, and Evaluating the Model
- This deep-learning neural network model contains two hidden layers with 80 and 30 neurons respectively.
- To increase model performance, we are using the activation function `ReLU` for the hidden layers. 
- Since the output is a binary classification, we use the  `Sigmoid` activation function for the output layer.
- The optimizer is `adam` and the loss function is `binary_crossentropy` for the compilation.
- We were not able to achieve the target model performance since the model accuracy is under 75%, resulting in an insufficient score to predict the success  of charity donations. 

### Neural Network Optimization 
- To attempt to increase the performance of the model, we looked at feature `ASK_AMT` value counts for binning.
<p align="center">
 <img width="581" alt="Screen Shot 2022-04-06 at 10 46 37 PM" src="https://user-images.githubusercontent.com/94571150/162128880-87185fe9-b2bf-4a43-aa9a-369ae601896b.png"> 
</p>
This gave us an accuracy score of 73%, which shows barely any improvement from the previous model of 72.8%.
<br><br>

- Increased the number of neurons on one of the hidden layers, then we used a model with three hidden layers.
<p align="center">
<img width="612" alt="Screen Shot 2022-04-06 at 10 34 55 PM" src="https://user-images.githubusercontent.com/94571150/162127518-2380ccf7-e0ce-442a-a45b-0619773a353a.png"> 
</p>
This gave us an accuracy score of 72.7%, which shows no improvement from the previous model of 72.8%. 
<br><br>

- Tried a different activation function (`tanh`) but none of these steps helped improve the model's performance.
<p align="center">
<img width="603" alt="Screen Shot 2022-04-06 at 10 36 50 PM" src="https://user-images.githubusercontent.com/94571150/162127724-fd3774e9-ee1c-4c84-8fca-d7b47004c06c.png">
</p>
This gave us an accuracy score of 72.9%, which shows no improvement from the previous model of 72.8%.

## Summary
All in all, the deep learning neural network model did not reach the target of 75% accuracy despite optimization attempts. 
Due to this analysis being a binary classification model, we could also look at supervised machine learning models such as RandomForest. With this model we could join various decision trees and generate a classified output. We could then evaluate the performance of this model against our deep learning neural network model.
