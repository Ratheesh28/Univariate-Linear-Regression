# Implementation of Univariate Linear Regression
## Aim:
To implement univariate Linear Regression to fit a straight line using least squares.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Get the independent variable X and dependent variable Y.
2.	Calculate the mean of the X -values and the mean of the Y -values.
3.	Find the slope m of the line of best fit using the formula.
 ![eqn1](./eq1.jpg)
4.	Compute the y -intercept of the line by using the formula:
![eqn2](./eq2.jpg)  
5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
```
#Program to find Univariate Linear Regression
#Developed by: RATHEESHKUMAR B R
#Register number: 212223110040

import numpy as np 
import matplotlib.pyplot as plt
x = np.array(eval(input()))
y = np.array(eval(input()))

xmean = np.mean(x)
ymean = np.mean(y)
num=0
den=0
for i in range(len(x)):
    num+=(x[i]-xmean)*(y[i]-ymean)
    den+=(x[i]-xmean)**2
m = num/den
b = ymean - m*xmean
print(m,b)
ypred = m*x+b
print(ypred)

plt.scatter(x,y,color='GREEN')
plt.plot(x,ypred,color='BLACK')
plt.show()


```
## Output
![alt text](<WhatsApp Image 2024-05-07 at 08.38.47_d5f10e9f.jpg>)

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
