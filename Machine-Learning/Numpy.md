#Numpy

The main algorithm of machine learning is based on linear algebra and statistics, etc. Numpy, which means numerical Python, is a representative package that helps make it easier to create linear algebra-based programs in Python.

Numpy offers compatible APIs based on low-level languages such as C/C++. Numpy guarantees very fast array operations, but the performance of the Python language itself is limited, so performance-critical parts can be integrated by writing them in C/C++-based code and calling them in Numpy.

It provides data handling as well as array-based operations. This is due to the fact that many machine learning algorithms are built on the basis of Numpy, as well as the input and output data of these algorithms, are used as Numpy array types.

# How to use np.array()

Return ndarray if you enter the object you want to convert to ndarray as a factor
ndarray.shape represents the dimensions and sizes of the ndarray in tuple form.

#  Reshape() to change the dimension and size of the ndarray
An error will occur if the change to the specified size is not possible.
If the factor is applied to -1, it is converted to a new shape compatible with the original ndarray