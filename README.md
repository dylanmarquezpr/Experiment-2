# Experiment 2 - Numerical Python

#### Name : Dylan Rvy A. Marquez 
#### Section : 2ECE-B 
#### Date : 08/25/2025

## OVERVIEW

This experiment focuses on using NumPy to perform mathematical preprocessing and array manipulations. It covers two problems: Normalization and Divisible by 3. The Normalization Problem introduces the concept of centering and scaling data, a key preprocessing step in data analytics. The Divisible by 3 Problem involves creating a structured 10×10 ndarray and applying filtering techniques to extract values that meet specific conditions. Together, these tasks strengthen the understanding of NumPy functions such as mean(), std(), random number generation, array reshaping, and element-wise operations.

### 1. NORMALIZATION PROBLEM 

The Normalization Problem demonstrates how to preprocess data by subtracting the mean and dividing by the standard deviation. This ensures that the data has a mean of 0 and a standard deviation of 1. In Python, this is achieved using numpy.mean() and numpy.std() functions.

#### PROCEDURE: 

1. Import NumPy.
 ```python
import numpy as np
 ```

2. Create a random 5×5 ndarray stored in variable X.
 ```python
X = np.random.rand(5, 5)
 ```
3. Compute the mean and standard deviation of X.
   
```python
mean = X.mean()
std = X.std()
 ```

4. Normalize the ndarray using the formula : Z = X−X / σ

```python
X_normalized = (X - mean) / std
 ```

5. Save the normalized ndarray as X_normalized.npy.

```python
 np.save("X_normalized.npy", X_normalized)
 ```

#### OUTPUT:

The output is a 5×5 ndarray where each value is normalized, resulting in data centered around 0 with unit variance.

### 2. DIVISIBLE BY 3 PROBLEM
The Divisible by 3 Problem involves generating the squares of the first 100 positive integers, arranging them into a 10×10 ndarray, and filtering the values divisible by 3. This applies the concepts of array creation, reshaping, and boolean indexing.

#### PROCEDURE:

1. Generate squares of integers from 1 to 100.
```python
squares = np.arange(1, 101) ** 2
 ```
3. Reshape the result into a 10×10 ndarray A.
   
```python
A = squares.reshape(10, 10)
 ``` 
5. Apply a condition to extract values divisible by 3.
   
 ```python
div_by_3 = A[A % 3 == 0]
 ```
7. Save the extracted values as div_by_3.npy.

```python
np.save("div_by_3.npy", div_by_3)
 ```

#### OUTPUT:


The program outputs the 10×10 ndarray of squares, followed by a filtered array containing only values divisible by 3. These results demonstrate efficient data handling using NumPy’s array operations.




