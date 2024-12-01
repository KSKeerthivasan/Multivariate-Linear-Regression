# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
<br> Load independent variables (X) and the dependent variable (y).
### Step2
<br>Add intercept term: Add a column of ones to X for the intercept.
### Step3
<br>Use the formula β = (X^T X)^(-1) X^T y to compute the regression coefficients.
### Step4
<br>Compute predictions using y_pred = X * β.
### Step5
<br>Calculate performance metrics like Mean Squared Error (MSE) or R-squared.
## Program:
```
import pandas as pd
from sklearn import linear_model
df = pd.read_csv("C:\\Users\\Keerthivasan\\Downloads\\carsemmision.csv")
df
```
```
X = df[['Weight', 'Volume']]
y = df['CO2']
regr = linear_model.LinearRegression()
regr.fit(X, y)
print('Coefficients:', regr.coef_)
print('Intercept:',regr.intercept_)
predictedCO2 = regr.predict([[3300, 1300]])
print('Predicted CO2 for the corresponding weight and volume',predictedCO2)
```
## Output:
<br>![Screenshot 2024-12-01 172358](https://github.com/user-attachments/assets/f45056bd-4dd9-4f90-9a54-6baa5287c5ef)
<br>![Screenshot 2024-12-01 172423](https://github.com/user-attachments/assets/7526d6ea-8077-4932-b94f-3f6006e1c8fa)
## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
