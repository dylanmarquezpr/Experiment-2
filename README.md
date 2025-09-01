# Experiment 2 - Numerical Python

#### Name : Dylan Rvy A. Marquez 
#### Section : 2ECE-B 
#### Date : 08/25/2025

## OVERVIEW

This experiment focuses on using NumPy to perform mathematical preprocessing and array manipulations. It covers two problems: Normalization and Divisible by 3. The Normalization Problem introduces the concept of centering and scaling data, a key preprocessing step in data analytics. The Divisible by 3 Problem involves creating a structured 10×10 ndarray and applying filtering techniques to extract values that meet specific conditions. Together, these tasks strengthen the understanding of NumPy functions such as mean(), std(), random number generation, array reshaping, and element operations.

### 1. NORMALIZATION PROBLEM 

The Normalization Problem demonstrates how to preprocess data by subtracting the overall mean and dividing by the overall standard deviation of the matrix. This process transforms the values so that the resulting matrix has a mean close to 0 and a standard deviation of 1. In Python, this is implemented using the built-in array methods .mean() and .std() applied directly to the matrix.

#### PROCEDURE: 

1. Import NumPy.
   
 ```python
import numpy as np  
 ```

2. Generate a random 5×5 matrix with values between 0 and 1.
   
 ```python
random_matrix = np.random.rand(5, 5)
 ```

3. Compute the mean and standard deviation of X.
   
```python
matrix_mean = random_matrix.mean() 
matrix_std = random_matrix.std() 
 ```

4. Normalize the ndarray using the formula : Z = X−X / σ

```python
normalized_matrix = (random_matrix - matrix_mean) / matrix_std
 ```

5. Save the normalized ndarray as X_normalized.npy.

```python
np.save("normalized_matrix.npy", normalized_matrix)
```

6. Print both the original random matrix and the normalized result.

```python
print("Original Random Matrix:\n", random_matrix) #print the original values
print("\nNormalized Matrix:\n", normalized_matrix) #print the normalized values
```

#### OUTPUT:

<img width="520" height="237" alt="Screenshot 2025-09-01 163544" src="https://github.com/user-attachments/assets/7b0727b7-45de-40d6-a5e2-6b4a62c3d157" />


The output first shows the original random 5×5 matrix with values between 0 and 1. It then displays the normalized matrix, where the values are adjusted so that the overall mean is approximately 0 and the standard deviation is 1.

### 2. DIVISIBLE BY 3 PROBLEM
The Divisible by 3 Problem involves generating the squares of the first 100 positive integers, arranging them into a 10×10 ndarray, and filtering the values divisible by 3. This applies the concepts of array creation, reshaping, and boolean indexing.

#### PROCEDURE:
1. Import the NumPy library.

```python
import numpy as np
 ```

2. Create a 10×10 matrix of the squares of the first 100 integers using arange() and reshape()
   
```python
X = (np.arange(1, 101) ** 2).reshape(10, 10)
print("Original 10x10 Matrix (Squares of 1–100):\n", X)
 ```

3. Extract numbers that are divisible by 3 using modulo and boolean indexing.
   
```python
div_by_3 = X[X % 3 == 0] 
print("\n The numbers divisible by 3:(Squares of 1–100)\n", div_by_3)
 ```

4. Save the filtered array into a .npy file.
   
 ```python
np.save("div_by_3.npy", div_by_3) 
print("\n Numbers divisible by 3 saved as 'div_by_3.npy'")

 ```

#### OUTPUT:

<img width="583" height="325" alt="Screenshot 2025-09-01 163557" src="https://github.com/user-attachments/assets/98879a4f-0af5-41a7-ba67-6208f4365acf" />


The output first displays the 10×10 matrix containing the squares of the numbers from 1 to 100. It then lists only the values divisible by 3, extracted into a separate 1D array and saved as div_by_3.npy.


## CONCLUSION 

The experiment is a demonstration of the practical use of NumPy in simplifying mathematical array manipulations and computation. The Normalization Problem showed how data can be standardized for consistency in analysis, while the Divisible by 3 Problem showcased array creation and conditional filtering. Together, these exercises really showed of how is NumPy in handling numerical tasks that would otherwise be tedious to perform manually.



