# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to predict the marks scored by a student using the simple linear regression model.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the standard Libraries.
2.Set variables for assigning dataset values.

3.Import linear regression from sklearn.

4.Assign the points for representing in the graph.

5.Predict the regression for marks by using the representation of the graph.

6.Compare the graphs and hence we obtained the linear regression for the given data

## Program:
```
/*
Program to implement the simple linear regression model for predicting the marks scored.
Developed by: KEERTHANA R
RegisterNumber:  212224040156
*/
```
```
import matplotlib.pyplot as plt

X = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12]
Y = [18, 28, 35, 45, 52, 60, 68, 74, 79, 85, 90, 94]

n = len(X)

mean_x = sum(X) / n
mean_y = sum(Y) / n

num = 0
den = 0
for i in range(n):
    num += (X[i] - mean_x) * (Y[i] - mean_y)
    den += (X[i] - mean_x) ** 2

m = num / den
b = mean_y - m * mean_x

print(f"Y = {m:.2f}X + {b:.2f}")

y_pred = [m * x + b for x in X]

plt.scatter(X, Y)
plt.plot(X, y_pred)
plt.xlabel("Study Hours")
plt.ylabel("Marks Scored")
plt.title("Simple Linear Regression with Realistic Data")
plt.show()
```
## Output:


<img width="952" height="678" alt="image" src="https://github.com/user-attachments/assets/634bc12b-1c5a-4d5c-90bd-e14b514b7a50" />

## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
