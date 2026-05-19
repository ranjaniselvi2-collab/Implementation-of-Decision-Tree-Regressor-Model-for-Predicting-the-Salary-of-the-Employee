# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

1. Import the required libraries.

2. Create the dataset and convert it into a DataFrame.

3. Separate the input feature (`StudyHours`) and target variable (`Marks`).

4. Split the dataset into training and testing data.

5. Create and train the `DecisionTreeRegressor` model using the training data.


## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: Ranjani S
RegisterNumber:212225230224
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.model_selection import train_test_split
from sklearn.tree import DecisionTreeRegressor, plot_tree
from sklearn.metrics import mean_squared_error, mean_absolute_error, r2_score

# Dataset
data = {
    'StudyHours': [1, 2, 3, 4, 5, 6, 7, 8, 9, 10],
    'Marks': [35, 40, 45, 50, 60, 68, 75, 82, 90, 98]
}

# Create DataFrame
df = pd.DataFrame(data)

# Features and Target
X = df[['StudyHours']]
y = df['Marks']

# Split the dataset
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)

# Create Decision Tree Regressor
model = DecisionTreeRegressor(random_state=42)

# Train the model
model.fit(X_train, y_train)

# Predict the test data
y_pred = model.predict(X_test)

# Evaluation Metrics
print("Mean Squared Error (MSE):", mean_squared_error(y_test, y_pred))
print("Mean Absolute Error (MAE):", mean_absolute_error(y_test, y_pred))
print("R2 Score:", r2_score(y_test, y_pred))

# Decision Tree Diagram
plt.figure(figsize=(12, 6))

plot_tree(
    model,
    feature_names=['StudyHours'],
    filled=True,
    rounded=True
)

plt.title("Decision Tree Regressor - Marks Prediction")
plt.show()

*/
```

## Output:

<img width="1137" height="581" alt="Screenshot 2026-05-19 144622" src="https://github.com/user-attachments/assets/a1af4235-3f39-45eb-b01b-60b6a65ad456" />


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
