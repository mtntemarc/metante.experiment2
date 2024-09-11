# metante.experiment2
EXPERIMENT 2 - Numerical Python

# Normalization Problem 
```
#Normalization Problem 

#Import Numpy Library
import numpy as np

#Start Program
#Create 5x5 ndarray with random values
X = np.random.rand(5, 5)

#Calculate the element-wise mean and standard deviation
mean_X = X.mean()
std_X = X.std()

#Check for standard deviation to avoid division by zero
if std_X == 0:
    print("Standard deviation is zero, normalization cannot be performed.")
else:
    #Normalize Array 
    X_normalized = (X - mean_X) / std_X
    
    #Save the normalized array to a .npy file
    np.save('X_normalized.npy', X_normalized)

    #Output: Original and Normalized Array
    print("Original Array:\n", X)
    print("\nNormalized Array:\n", X_normalized)

    #Load and verify the saved normalized array
    loaded_X_normalized = np.load('X_normalized.npy')
    print("\nLoaded Normalized Array from File:\n", loaded_X_normalized)
```
# Divisible by 3 Problem 
 ```
#Divisible by 3 Problem 

#Import Numpy Library
import numpy as np  

#Start Program
#Create 10x10 ndarray of squares of integers from 1 to 100
A = np.arange(1, 101)**2
A = A.reshape((10, 10))  # Reshape into a 10x10 array

#Output: 10x10 array
print("10x10 Array of Squares of the First 100 Positive Integers:\n", A)

#Determine elements divisible by 3 using modulo operation
div_by_3 = A[A % 3 == 0]

#Output: Elements divisible by 3
print("\nElements Divisible by 3:\n", div_by_3)

#Check if there are no elements divisible by 3 (edge case)
if div_by_3.size == 0:
    print("\nNo elements divisible by 3 were found in the array.")
else:
    #Save results to a .npy file
    np.save('div_by_3.npy', div_by_3)
```
    
