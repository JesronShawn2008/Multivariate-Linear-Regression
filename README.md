# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1: Import the required libraries (pandas and sklearn.linear_model). Read the dataset containing the independent variables (features like Weight and Volume) and the dependent target variable (CO2).
### Step2: Split the dataset by assigning the independent columns (Weight and Volume) to the feature matrix X, and the dependent column (CO2) to the target vector y.
### Step3: Initialize the linear regression model using linear_model.LinearRegression() and fit the model onto the training data (X and y) to calculate the coefficients and intercept.
### Step4: Pass new input data (e.g., specific values for Weight and Volume) into the trained model's predict function, then print the regression coefficients, intercept, and the final predicted {CO2} value.

## Program:
```
import pandas as pd
from sklearn import linear_model
df = pd.read_csv("car (1).csv")
X = df[['Weight', 'Volume']]
y = df['CO2']
regr = linear_model.LinearRegression()
regr.fit(X, y)
print('Coefficients:', regr.coef_)
print('Intercept:', regr.intercept_)
input_data = pd.DataFrame({'Weight': [3300], 'Volume': [1300]})
predictedCO2 = regr.predict(input_data)
print('Predicted CO2 for the corresponding weight and volume:', predictedCO2)
```
## Output:
<img width="723" height="91" alt="image" src="https://github.com/user-attachments/assets/52fe7c51-4391-4f80-9c62-d817188c7321" />


## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
