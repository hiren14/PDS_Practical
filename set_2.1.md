# 1 Write a NumPy program to create an element-wise comparison (greater, greater_equal, less, and less_equal) of two given arrays.


```python
import numpy as np

```


```python
arr1=np.array([1,2,3])
arr2=np.array([4,5,6])
g= np.greater(arr1,arr2)
print(g)

```

    [False False False]
    


```python
gl= np.greater_equal(arr1,arr2)
print(gl)

```

    [False False False]
    


```python
l= np.less(arr1,arr2)
print(l)
```

    [ True  True  True]
    


```python
le= np.less_equal(arr1,arr2)
print(le)
```

    [ True  True  True]
    

# 2 Write a NumPy program to create a null vector of size 10 and update the sixth value to
11. 
##### [ 0. 0. 0. 0. 0. 0. 0. 0. 0. 0.]
##### Update sixth value to 11
##### [ 0. 0. 0. 0. 0. 0. 11. 0. 0. 0.] 



```python
zero=np.zeros(10)
print(zero)
```

    [0. 0. 0. 0. 0. 0. 0. 0. 0. 0.]
    


```python
zero[6]=11
print(zero)

```

    [ 0.  0.  0.  0.  0.  0. 11.  0.  0.  0.]
    

# 3 Write a NumPy program to find common values between two arrays.
##### Expected Output:
##### Array1: [ 0 10 20 40 60]
##### Array2: [10, 30, 40]
##### Common values between two arrays:
##### [10 40] 



```python
arr=np.array([0,10,20,40,60])
arrr1=np.array([10,30,40])
ar_com=np.intersect1d(arr,arrr1)
print(ar_com)
```

    [10 40]
    

# 4 Write a NumPy program to create a new shape to an array without changing its data.
#### Reshape 3x2:
#### [[1 2]
#### [3 4]
#### [5 6]]
#### Reshape 2x3:
#### [[1 2 3]
#### [4 5 6]]


```python
arr=np.array([[0,10],[20,40],[60,70]])
print(arr.shape)
x=np.reshape(arr,(2,3))
print(x)
print(x.shape)
```

    (3, 2)
    [[ 0 10 20]
     [40 60 70]]
    (2, 3)
    

# 5. Write a NumPy program to Generate matrix using random integers between 10 and 30 



```python
array = np.random.randint(10,30, size=(5, 5))
print(array)
```

    [[18 19 19 24 23]
     [28 19 29 15 14]
     [20 14 17 11 26]
     [26 21 18 26 19]
     [20 15 10 29 18]]
    

# 6. Write a NumPy program to Shuffle numbers between 0 and 10 


```python
arr = np.arange(0,10)
print(arr)
np.random.shuffle(arr)
print(arr)
```

    [0 1 2 3 4 5 6 7 8 9]
    [1 4 3 8 7 6 0 9 5 2]
    

# 8 Write a NumPy program to round elements of the array to the nearest integer. 


```python
arr=np.array([1.21,33.23,55.5,88.8,99.9],dtype='float')
arr_ro=np.round(arr)
print(arr_ro)

```

    [  1.  33.  56.  89. 100.]
    

# Write a NumPy program to count the number of days and number of weekdays in August 2022. 



```python

days = np.datetime64('2022-09-01') - np.datetime64('2022-08-01')
print(f"Total Number of days in August 2022: {days}") 
weekdays = np.busday_count('2022-08-01', '2022-09-01')
print(f"Total Number of weekdays in August 2022: {weekdays}")  
```

    Total Number of days in August 2022: 31 days
    Total Number of weekdays in August 2022: 23
    

# 10. Write a NumPy program to perform rowwise and column wise sorting of given array. 


```python
arr = np.random.randint(10,30, size=(2, 2))
print('row wise ')
ar_row=np.sort(arr,axis=1)
print(ar_row)
print()
ar_col=np.sort(arr,axis=0)
print(ar_col)
```

    row wise 
    [[20 22]
     [16 18]]
    
    [[16 18]
     [20 22]]
    

# 11. Write a NumPy program to find Rowwise and column wise maximum from two matrix 


```python
arr = np.random.randint(10,30, size=(2, 2))
print('row wise max')
ar_row=np.max(arr,axis=1)
print(ar_row)
print()
print('col wise max')
ar_col=np.max(arr,axis=0)
print(ar_col)

```

    row wise max
    [26 14]
    
    col wise max
    [26 19]
    

# 12. Write a NumPy program to capitalize the first letter, lowercase, uppercase, swapcase,title-case of all the elements of a given array. 


```python
x=input("enter a string")
up=np.char.upper(x)
print(up)
lo=np.char.lower(x)
print(lo)
cap=np.char.capitalize(x)
print(cap)
swap=np.char.swapcase(x)
print(swap)
ti=np.char.title(x)
print(ti)
```

    enter a stringHiren Lalani
    HIREN LALANI
    hiren lalani
    Hiren lalani
    hIREN lALANI
    Hiren Lalani
    


```python

```
