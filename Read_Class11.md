# JupyterLab
JupyterLab is the latest web-based interactive development environment for notebooks, code, and data. Its flexible interface allows users to configure and arrange workflows in data science, scientific computing, computational journalism, and machine learning. A modular design invites extensions to expand and enrich functionality.

[instructions of using JupyterLab](https://jupyterlab.readthedocs.io/en/stable/getting_started/overview.html)

# NumPy data analysis
NumPy is a commonly used Python data analysis package that is used to speed up the workflow, and interface with other packages in Pythons ecosystem.

[Numpy cheat sheet](https://s3.amazonaws.com/dq-blog-files/numpy-cheat-sheet.pdf)
- ssv (semicolon separated values) format

## 2-Dimensional Arrays
In a NumPy array, the number of dimensions is called the rank, and each dimension is called an axis. So the rows are the first axis, and the columns are the second axis.
- One of the limitations of NumPy is that all the elements in an array have to be of the same type.

### Creating A NumPy Array
We can create a NumPy array using the numpy.array function. If we pass in a list of lists, it will automatically create a NumPy array with the same number of rows and columns
```
imoprt numpy as np
```

### Alternative NumPy Array Creation Methods
### using numpy.zeros  -->  creates an array with elements of value zero

 --> this will create a 3 rows 4 columns array with all elements = 0
 
```
empty_array = np.zeros((3,4))
``` 
```
np.zeros(5)
array([ 0.,  0.,  0.,  0.,  0.])
```
```
np.zeros((2, 1))
array([[ 0.],
       [ 0.]])
```
```
s = (2,2)
np.zeros(s)
array([[ 0.,  0.],
       [ 0.,  0.]])
```

### using numpy.random.rand 

--> Generate a 2 x 4 array of ints between 0 and 4, inclusive:
```
np.random.randint(5, size=(2, 4))
array([[4, 0, 2, 1],
       [3, 2, 2, 0]])
```

### using the numpy.genfromtxt function.

--> We can use it to read in our initial data on red wines.

example:
-Use the genfromtxt function to read in the winequality-red.csv file.
-Specify the keyword argument delimiter=";" so that the fields are parsed properly.
-Specify the keyword argument skip_header=1 so that the header row is skipped.
```
wines = np.genfromtxt("winequality-red.csv", delimiter=";", skip_header=1)
```

- the index of the first row is 0, and the index of the first column is 0.
-  We can use array indexing to select individual elements, groups of elements, or entire rows and columns.

### Slicing NumPy Arrays
- wines[0:3,3]  --> returns the element in the third column of each row up to the third row its not concluded.

### Assigning Values To NumPy Arrays
- wines[1,5] = 10
- wines[:,10] = 50

## 1-Dimensional NumPy Arrays
looks like this
```
11.200
0.280
0.560
1.900
0.075
17.000
60.000
0.998
3.160
0.580
9.800
6.000
```
```
np.random.rand(3)
```

## N-Dimensional NumPy Arrays
 list of lists of lists.
 
## NumPy Data Types
NumPy is written in a programming language called C, which stores data differently than the Python data types.

### Converting Data Types
- use the numpy.ndarray.astype.

--> to convert an array to a different type. copies and returns new array with specified data type
- wines.astype(int)

 --> create NumPy dtype objects like numpy.int32:
 - np.int32
 - wines.astype(np.int32)


## NumPy Array Operations
regular operations can be applied to numpy arrays

## Reshaping NumPy Arrays


- using numpy.transpose
```
np.transpose(wines).shape
```
--> rows become columns, and vice versa

-using numpy.ravel
```
array_one = np.array(
    [
        [1, 2, 3, 4],
        [5, 6, 7, 8]
    ]
)
array_one.ravel()
``` 
output --> array([1, 2, 3, 4, 5, 6, 7, 8])


-using numpy.reshape 
```
wines[1,:].reshape((2,6))
```
--> will turn the second row of wines into a 2-dimensional array with 2 rows and 6 columns:

[More](https://www.dataquest.io/blog/numpy-tutorial-python/)
