# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required libraries and create the employee salary dataset.

2. Select the input feature (Experience) and target variable (Salary).

3. Split the dataset into training data and testing data.

4. Train the Decision Tree Regressor model using the training data.

5. Predict the salary using test data and evaluate the model performance.


## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: Ranjani S
RegisterNumber:212225230224

import pandas as pd
import matplotlib.pyplot as plt
from sklearn.tree import DecisionTreeRegressor
from sklearn.model_selection import train_test_split
from sklearn.metrics import mean_squared_error

# Employee dataset
data = {
    'Experience': [1, 2, 3, 4, 5, 6, 7, 8, 9, 10],
    'Salary': [25000, 30000, 35000, 40000, 50000,
               60000, 65000, 70000, 80000, 90000]
}

# Create DataFrame
df = pd.DataFrame(data)

# Features and Target
X = df[['Experience']]
y = df['Salary']

# Train-Test Split
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)

# Model Creation
model = DecisionTreeRegressor(random_state=42)
model.fit(X_train, y_train)

# Prediction
y_pred = model.predict(X_test)

# Evaluation
print("Mean Squared Error:", mean_squared_error(y_test, y_pred))

# Graph
plt.scatter(X, y)
plt.plot(X, model.predict(X), linewidth=2)
plt.title("Decision Tree Regressor")
plt.xlabel("Experience")
plt.ylabel("Salary")
plt.show()
 
*/
```

## Output:

<img width="716" height="497" alt="Screenshot 2026-05-11 194747" src="https://github.com/user-attachments/assets/60877499-4397-4346-ba14-2c1f39d02759" />


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
