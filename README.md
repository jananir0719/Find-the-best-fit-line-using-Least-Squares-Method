# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula. 
4. Compute the y -intercept of the line by using the formula:
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:
```
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: JANANI R
RegisterNumber:  25018734
*/
import numpy as np
import matplotlib.pyplot as plt

# Sample dataset (Univariate)
x = np.array([1, 2, 3, 4, 5])     # Input feature
y = np.array([2, 4, 5, 4, 5])     # Target values

# Number of observations
n = len(x)

# Calculate slope (m) and intercept (c)
m = (n * np.sum(x * y) - np.sum(x) * np.sum(y)) / (n * np.sum(x ** 2) - (np.sum(x)) ** 2)
c = (np.sum(y) - m * np.sum(x)) / n

print(f"Slope (m): {m}")
print(f"Intercept (c): {c}")

# Predict y values
y_pred = m * x + c

# Plot the data points and regression line
plt.scatter(x, y, color='blue', label='Actual data')
plt.plot(x, y_pred, color='red', label='Fitted line')
plt.xlabel('X')
plt.ylabel('Y')
plt.title('Univariate Linear Regression using Least Squares')
plt.legend()
plt.show()

```

## Output:
 
<img width="305" height="67" alt="image" src="https://github.com/user-attachments/assets/9714286d-de09-466f-b0c8-0eb6c614b393" />
<img width="996" height="747" alt="image" src="https://github.com/user-attachments/assets/a1e94b01-55ef-4ffc-9111-b341ab5b916e" />





## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.


