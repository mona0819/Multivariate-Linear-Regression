# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
Import the required libraries such as Pandas and Scikit-learn to handle data and perform linear regression.

### Step2
Read the cars.csv file using Pandas and store it in a dataframe.

### Step3
Select Weight and Volume as independent variables (X) and CO2 as the dependent variable (y).

### Step4
Create a linear regression model and train it using the dataset with the fit() function.

### Step5
Give new input values for Weight = 3300 and Volume = 1300, then use the trained model to predict the CO2 emission and display the result.

## Program:
```
Developed by: Mohana Priya D
Register Number: 212225230182
```
```python
import pandas as pd
from sklearn import linear_model
df = pd.read_csv("carsemission.csv")
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
<img width="742" height="126" alt="image" src="https://github.com/user-attachments/assets/4d103ced-6f2b-4eee-b591-e10f06d76ca7" />

## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
