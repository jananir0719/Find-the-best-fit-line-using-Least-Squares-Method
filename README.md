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
 
# Preprocessing Input data 
 
X = np.array([1,2,3,4,5,6,7,8,9,10]) 
Y = np.array([0,3,5,7,9,11,13,2,4,8]) 
 
# Mean 
X_mean =np.mean(X) 
Y_mean=np.mean(Y) 
num=0  #for slope 
denom=0  #for slope 
 
#to find sum of (xi-x') & (yi-y') & (xi-x')^2 
for i in range(len(X)): 
    num+=(X[i] -X_mean)*(Y[i]-Y_mean) 
    denom+= (X[i]-X_mean)**2 
     
#calculate slope 
m=num/denom 
 
#calculate intercept 
b=Y_mean-m*X_mean 
 
print(m,b) 
#Line equation 
y_predicted=m*X+b 
print(y_predicted) 
#to plot graph 
plt.scatter(X,Y) 
plt.plot(X,y_predicted,color='red') 
plt.show()

```

## Output:
 
<img width="953" height="772" alt="image" src="https://github.com/user-attachments/assets/b194fcb2-4b25-4846-a039-1e257e0efbee" />





## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.


