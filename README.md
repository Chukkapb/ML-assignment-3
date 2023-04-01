# ML-assignment-3
Assignment 3
Bhargavi Chukkapalli (700743393)

# 1.a.1)Creating random vector of size 15 having only Integers in the range 1-20.
To create a random vector of given size using python , we can import numpy library and use random function
import numpy as np
v =  np.random.randint(1,20,(15,))
print(v)

#1.a.2). Reshaping the array to 3 by 5 
to reshape an array we can use reshape() function
arr = v.reshape(3,5)
print(arr.shape)
print(arr)

#1.a.3).Replacing the max in each row by 0
consider each row of the matrix ,find the max element of the row and replace it with zero (axis=1 is used to consider each row from the matrix)
row_max = arr.max(axis=1).reshape(-1,1)
arr = np.where(arr == row_max, 0, arr)
print('\n',arr)

#Create a 2-dimensional array of size 4 x 3 (composed of 4-byte integer elements), also print the shape, type and data type of the array
to find the shape and data type of array , we can use shape and d.type() functions
x = np.array([[22, 41, 39], [62, 44, 35], [83, 9, 17], [11, 25, 27]], np.int32)
print('Shape:', x.shape)
print('Type:', type(x))
print('Data type:', x.dtype)

#Write a program to compute the eigenvalues and right eigenvectors of a given square array given below:
to find eig values we have to import linalg function from numpy library
from numpy import linalg as l
arr1 = np.array([[3, -2], [1, 0]], np.int32)
e, r = l.eig(arr1)
print('Eigenvalues:', e)
print('\nRight eigenvectors:\n', r)

#Compute the sum of the diagonal element of a given array
sum of diagonal elements of a matrix is called trace, There is a built in function trace() to find the sume of diagonal elements of a matrix
arr2 = np.array([[0, 1, 2], [3, 4, 5]])
res = np.trace(arr2)
print('Sum of diagonal elements:', res)

#Write a NumPy program to create a new shape to an array without changing its data. 
we can change the shape of the matrix without changing the data as long as the size of matrix doesn't change
w = np.arange(1,7).reshape(3,2)
print(w)
v = w.reshape(2,3)
print(v)

#Write a Python programming to create a below chart of the popularity of programming Languages.
to plot or graph, we import matplotlib library
import matplotlib.pyplot as plt
languages = ['Java', 'Python', 'PHP', 'JavaScript', 'C#', 'C++']
popularity = np.array([22.2, 17.6, 8.8, 8, 7.7, 6.7])
exp = [0.1, 0, 0, 0, 0, 0]
plt.pie(popularity, labels = languages, explode = exp, shadow = True, autopct='%1.1f%%', startangle = 135)
plt.show()
