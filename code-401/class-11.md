# NumPy Tutorial: Data Analysis with Python

### CSV Data
to work with the data using Python and the csv package. We can read in the file using the csv.reader object
```python
import csv
with open('fille_name.csv', 'r') as f:
    data = list(csv.reader(f, delimiter=';'))
```

### Numpy 2-Dimensional Arrays
In a NumPy array, the number of dimensions is called the rank, and each dimension is called an axis. So the rows are the first axis, and the columns are the second axis.

We can create a NumPy array using the `numpy.array` function
>One of the limitations of NumPy is that all the elements in an array have to be of the same type.

You can check the number of rows and columns in our data using the shape property of NumPy arrays.

### Using NumPy To Read In Files
to use NumPy to directly read csv or other files into arrays. We can do this using the numpy.genfromtxt function.
```python
import numpy as np
data = np.genfromtxt("file_name.csv", delimiter=";", skip_header=1)
```

### NumPy Data Types
NumPy stores values using its own data types, which are distinct from Python types.This is because the core of NumPy is written in a programming language called C, which stores data differently than the Python data types.

```python
data.dtype
```

### Converting Data Types
```python
data.astype(int) #int64
data.astype(np.int32)
```

### Broadcasting
Unless the arrays that you’re operating on are the exact same size, it’s not possible to do elementwise operations. In cases like this, NumPy performs broadcasting to try to match up elements. Essentially, broadcasting involves a few steps:

- The last dimension of each array is compared.
    -    If the dimension lengths are equal, or one of the dimensions is of length 1, then we keep going.
    -   If the dimension lengths aren’t equal, and none of the dimensions have length 1, then there’s an error.
- Continue checking dimensions until the shortest array is out of dimensions.
