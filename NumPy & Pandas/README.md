# Data Analysis Using NumPy & Pandas

## NumPy:
1. It is super important for multi-dimensional array library for scientific computing.
2. Almost all the other libraries in the PyData ecosystem rely on NumPy Library as their main building block. 
3. It is implemented in C & Forton for faster processing. 


Applications:
 - For pure mathematical calculations  - MATLAB, SciPy 
 - For plotting used by Matplotlib
 - Backend of Pandas, connect4, digital Photography 
 - Machine Learning - directly or indirectly - the ideas of Tensors are connected to NumPy
 
Arrays: Collection of elements of same type. 
 - Vectors  - strictly one dimensional
 - Matrices - are two dimensional, but they can have either row/ column only. 

>
>NumPy Arrays v/s List
>
>NumPy arrays are fast while the Python in-built list slow because:
>
 > - This is because the list can store element of different datatypes, while NumPy can have only one type of data in a array. Hence NumPy does not do type checking every time and hence faster. 
 > - Since the array are homogeneous, every item takes up the same size of the block in the memory. 
 > - List also store other data related to elements like - size, frequency count, type etc and hence it uses more bytes of memory compared to NumPy.
 > - Numpy uses continuous memory (Contiguous), while list elements are scattered all over memory block. Hence List take longer memory lookups. Numpy Uses SIMD (Single Instruction Multiple Data) vector process to do computation simultaneously and use the cache effectively.
 >
 >List can't do the Element by Element computation which is supported by Numpy.


## Pandas:
There are two ways of creating Matplotlib plots!





