# Read 11: Data Analysis

## JupyterLab Releases

- JupyterLab is a next-generation web-based user interface for Project Jupyter.

- JupyterLab enables to work with documents and activities such as Jupyter notebooks, text editors, terminals, and custom components in a flexible, integrated, and extensible manner

**Code Consoles**: provide transient scratchpads for running code interactively, with full support for rich output

**Kernel-backed documents**: enable code in any text file to be run interactively in any Jupyter kernel.

# NumPy Tutorial: Data Analysis with Python

- NumPy is a commonly used Python data analysis package.
### Numpy 2-Dimensional Arrays / matrix

- rows: are the first axis.
- columns: are the second axis.
- Array function used to convert th list of lists into an array.

- Code Example:
```
    import csv
    with open("winequality-red.csv", 'r') as f:
        wines = list(csv.reader(f, delimiter=";"))
    import numpy as np
    wines = np.array(wines[1:], dtype=np.float)
```
### Alternative NumPy Array Creation Methods
 - Using _np.zeros_ where are all elements are zeroes.
```    
     import numpy as np 
     empty_array = np.zeros((3,4))
```
- Using _numpy.random.rand._ where each element is a random number
```
     np.random.rand(3,4)
```
### Using NumPy To Read In Files
- using _numpy.genfromtxt_ function.
```
wines = np.genfromtxt("winequality-red.csv", delimiter=";", skip_header=1)
```
### Indexing NumPy Arrays
- NumPy is zero-indexed, the index of the first row is 0, and the index of the first column is 0.
Ex: `wines[2,3]` 

### Slicing NumPy Arrays
- using colon, selects elements up until the last index, without it being included.
Ex: `wines[0:3,3]` 

- We can extract an entire column `_wines[:,3]_` or an entire row `_wines[3,:]_`
- We can choose the whole array using `_wines[:,:]_`

### Assigning Values To NumPy Arrays
`wines[1,5] = 10`


### NumPy Data Types
- using _array-name.dtype_
- Data type can be any of the following:
  - **float**: numeric floating point data.
    **int**: integer data.
    **string**: character data.
    **object**: Python objects.

### Data Type Conversions
- _array-name.astype(int)_

### NumPy Array Operations

#### Single Array Math

- basic mathematical operations `(/, \*, -, +, ^)` with an array and a value, it will apply the operation to each.of the elements in the array.

#### Multiple Array Math

- applying mathematical operations `(/, \*, -, +, ^)` between arrays.
