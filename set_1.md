# 1 Write a program in python to read two strings and display them on console. Use input ()  functions.



```python
a = input("Enter Your First Name:")
b = input("Enter Your SurName:")
print(a+" "+b)
```

    Enter Your First Name:Hiren 
    Enter Your SurName:Lalani
    Hiren  Lalani
    

# 2 Python Program to Print first N Fibonacci numbers 



```python
# Fibonacci Series
n = int(input("Enter How Many Elements You Want In Series: "))

n1 = 0
n2 = 1
count = 0
if n == 1:
    print(n1)
else:
    while count < n:
        print(n1, end=",")
        nth = n2 + n1
        n1, n2 = n2, nth
        count += 1

```

    Enter How Many Elements You Want In Series: 4
    0,1,1,2,

# 3 Python Program To check whether entered number is palindrome or not. 



```python
n=int(input("Enter number: "))
a=int(n)
c=str(n)
z=0
for i in range(len(c)): 
    y=int(n%10)
    n=n/10
    z=z*10+y
print(z)
if a==z:
     print("number is panindrome")
else:
     print("number is not panindrome")

```

    Enter number: 121
    121
    number is panindrome
    

# 4 Write a Python program to check if the number provided by the user is an Armstrong number. Perform it with and without user defined function. 



```python
def armstrong(d):
    z=0
    a=str(d)
    for i in range(len(a)):
        b=d%10
        d=int(d/10)
        z=z+b**len(a)
    return z
x=int(input("Enter a number: ")) 
c=int(x)
e=armstrong(c)
print(e)
if c==e:
    print("number is armstrong")
else:
    print("number is not armstrong")
```

    Enter a number: 153
    153
    number is armstrong
    

# 5 Write a Python program to print all Prime numbers in an Interval using user defined function 


```python
low = int(input("enter a lower "))
upper = int(input("enter upper "))
print("prime number betwwen {0} and {1}".format(low,upper)) 
for num in range(low,upper+1):
    if num>1:
        for i in range(2,num):
            if (num%i)==0:
                break
        else: 
            print(num)
```

    enter a lower 1
    enter upper 10
    prime number betwwen 1 and 10
    2
    3
    5
    7
    

# 6 Python Program for rotate the elements of array.



```python
#List slicing approch to rotate the array 
def array_rotate(a,d):
    n=len(a)
    a[:]=a[d:n] + a[0:d]
    return a
a= []
m = int(input("enter the number of elements"))

# iterating till the range 
for i in range(0,m):
    ele =int(input())
    a.append(ele)
print(a)
print("\n")
d = int(input("enter the roation value from which index"))
print(array_rotate(a,d))
```

    enter the number of elements5
    1
    2
    3
    4
    5
    [1, 2, 3, 4, 5]
    
    
    enter the roation value from which index2
    [3, 4, 5, 1, 2]
    

# 7 Python Program to Split the array and add the first part to the end of second part. 



```python
def array_spilt(arr,n,k):
    for i in range(0,k):
        x = arr[0]
        for j in range(0,n-1):
            arr[j] = arr[j+1]
        arr[n-1] = x
# main 
arr = []
m = int(input("enter the number of elements "))
# iltrating till range 
for i in range(0,m):
    ele = int(input())
    arr.append(ele)
#print(arr)
n = len(arr)
pos = int(input("enter the postion "))
array_spilt(arr,n,pos)
for i in range(0, n):
    print(arr[i], end = ' ')
```

    enter the number of elements 5
    1
    2
    3
    4
    5
    enter the postion 2
    3 4 5 1 2 

# 8 Python Program to check if given array is Monotonic or not.
##### Input : 6 5 4 4
##### Output : true
##### Input : 5 15 20 10
##### Output : false 



```python
def isMonotonic(A):
    return (all(A[i] <= A[i + 1]
                for i in range(len(A) - 1)) or
            all(A[i] >= A[i + 1] for i in range(len(A) - 1)))
# Driver program
A = []
m = int(input("enter the number of elements required "))
# iterating till loop
for i in range(0,m):
    ele = int(input())
    A.append(ele)
#printing arr
print(A)
# Print required result
print(isMonotonic(A))
```

    enter the number of elements required 5
    1
    2
    3
    5
    5
    [1, 2, 3, 5, 5]
    True
    

# 9 Python program to print even numbers and duplicate from a list 


```python
def even(arr):
    for x in arr:
        if x % 2 ==0:
            print(x,end=' ')

# checking condition
        
def duplicate(arr):
    n = len(arr)
    dup = []
    for i in range(n):
        k = i+1 
        for j in range(k,n):
            if(arr[i] == arr[j] and arr[i] not in dup):
                dup.append(arr[i])
#print(dup) 
    return dup
# main code
arr = []
m = int(input("enter the elements "))
# loop
for i in range(0,m):
    ele= int(input())
    arr.append(ele)
print(arr)
# calling even
print("even numbers are")
even(arr)
print("\nduplicate elements are",duplicate(arr))
```

    enter the elements 5
    1
    2
    6
    6
    2
    [1, 2, 6, 6, 2]
    even numbers are
    2 6 6 2 
    duplicate elements are [2, 6]
    

# 10 Python program to find N largest elements from a list
##### Input : [4, 5, 1, 2, 9]
##### N = 2
##### Output : [9, 5]
##### Input : [81, 52, 45, 10, 3, 2, 96]
##### N = 3
##### Output : [81, 96, 52] 



```python
#N largest elements
#function
def N_max_elements(list, N):
    result_list = []
    for i in range(0, N):
        maximum = 0
        for j in range(len(list)):
            if list[j] > maximum:
                maximum = list[j]
        list.remove(maximum)
        result_list.append(maximum)
    return result_list
#test 
list1 = []
m = int(input("enter number of elements "))
N = int(input('enter the max of elements '))
for i in range(0,m):
    ele = int(input())
    list1.append(ele)
print(list1) 
print(N, "max elements in ",list1)
# Calling and printing the function
print(N_max_elements(list1, N))
```

    enter number of elements 5
    enter the max of elements 2
    1
    55
    66
    44
    2
    [1, 55, 66, 44, 2]
    2 max elements in  [1, 55, 66, 44, 2]
    [66, 55]
    

# 11 Write a program to create a dictionary of student details and perform basic operation on it.


```python
students = dict()
n = int(input("Enter number of students :"))
for i in range(n):
    sname = input("Enter names of student :")
    marks= []
    for j in range(5):
        mark = float(input("Enter marks :"))
        marks.append(mark)
        students[sname] = marks
print("Dictionary of student created :")
print(students)
```

    Enter number of students :2
    Enter names of student :hi
    Enter marks :22
    Enter marks :2
    Enter marks :3
    Enter marks :55
    Enter marks :54
    Enter names of student :4
    Enter marks :44
    Enter marks :55
    Enter marks :55
    Enter marks :55
    Enter marks :55
    Dictionary of student created :
    {'hi': [22.0, 2.0, 3.0, 55.0, 54.0], '4': [44.0, 55.0, 55.0, 55.0, 55.0]}
    


```python

```
