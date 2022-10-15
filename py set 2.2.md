# 1 Write a Pandas program to read a CSV file from a specified source and print the first 10 rows.


```python
import pandas as pd

data = pd.read_csv("diamonds.csv")
print(data.head(10))
```

       carat        cut color clarity  depth  table  price     x     y     z
    0   0.23      Ideal     E     SI2   61.5   55.0    326  3.95  3.98  2.43
    1   0.21    Premium     E     SI1   59.8   61.0    326  3.89  3.84  2.31
    2   0.23       Good     E     VS1   56.9   65.0    327  4.05  4.07  2.31
    3   0.29    Premium     I     VS2   62.4   58.0    334  4.20  4.23  2.63
    4   0.31       Good     J     SI2   63.3   58.0    335  4.34  4.35  2.75
    5   0.24  Very Good     J    VVS2   62.8   57.0    336  3.94  3.96  2.48
    6   0.24  Very Good     I    VVS1   62.3   57.0    336  3.95  3.98  2.47
    7   0.26  Very Good     H     SI1   61.9   55.0    337  4.07  4.11  2.53
    8   0.22       Fair     E     VS2   65.1   61.0    337  3.87  3.78  2.49
    9   0.23  Very Good     H     VS1   59.4   61.0    338  4.00  4.05  2.39
    

# Write a Pandas program to read a dataset from diamonds Data Frame and print the last 6 rows. 



```python
import pandas as pd

data = pd.read_csv("diamonds.csv")
print(data.tail(6))
```

           carat        cut color clarity  depth  table  price     x     y     z
    53934   0.72    Premium     D     SI1   62.7   59.0   2757  5.69  5.73  3.58
    53935   0.72      Ideal     D     SI1   60.8   57.0   2757  5.75  5.76  3.50
    53936   0.72       Good     D     SI1   63.1   55.0   2757  5.69  5.75  3.61
    53937   0.70  Very Good     D     SI1   62.8   60.0   2757  5.66  5.68  3.56
    53938   0.86    Premium     H     SI2   61.0   58.0   2757  6.15  6.12  3.74
    53939   0.75      Ideal     D     SI2   62.2   55.0   2757  5.83  5.87  3.64
    

# Write a Pandas program to select a series from diamonds Data Frame. Print the content of the series


```python
import pandas as pd

data = pd.read_csv("diamonds.csv")
print(data['price'])
```

    0         326
    1         326
    2         327
    3         334
    4         335
             ... 
    53935    2757
    53936    2757
    53937    2757
    53938    2757
    53939    2757
    Name: price, Length: 53940, dtype: int64
    

# Write a Pandas program to find the number of rows and columns and the data type of each column of the diamonds Data frame. 


```python
import pandas as pd

data = pd.read_csv("diamonds.csv")
print(data.shape)
print(data.dtypes)
```

    (53940, 10)
    carat      float64
    cut         object
    color       object
    clarity     object
    depth      float64
    table      float64
    price        int64
    x          float64
    y          float64
    z          float64
    dtype: object
    

# Write a Pandas program to rename two of the columns of the diamonds Data frame. 


```python
import pandas as pd

data = pd.read_csv("diamonds.csv")
print(data.head(4))
data.rename(columns={'color': 'diamond_color', 'clarity': 'dimaond_clarity'}, inplace=True)
print(data.head(4))
```

       carat      cut color clarity  depth  table  price     x     y     z
    0   0.23    Ideal     E     SI2   61.5   55.0    326  3.95  3.98  2.43
    1   0.21  Premium     E     SI1   59.8   61.0    326  3.89  3.84  2.31
    2   0.23     Good     E     VS1   56.9   65.0    327  4.05  4.07  2.31
    3   0.29  Premium     I     VS2   62.4   58.0    334  4.20  4.23  2.63
       carat      cut diamond_color dimaond_clarity  depth  table  price     x  \
    0   0.23    Ideal             E             SI2   61.5   55.0    326  3.95   
    1   0.21  Premium             E             SI1   59.8   61.0    326  3.89   
    2   0.23     Good             E             VS1   56.9   65.0    327  4.05   
    3   0.29  Premium             I             VS2   62.4   58.0    334  4.20   
    
          y     z  
    0  3.98  2.43  
    1  3.84  2.31  
    2  4.07  2.31  
    3  4.23  2.63  
    

# Write a Pandas program to Sort the diamonds data based on length ascending and descending both


```python
import pandas as pd

data = pd.read_csv("diamonds.csv")
print(data.head(3))
ascending = data.sort_values(by='x', ascending=True)
print(ascending.head(3))
decending = data.sort_values(by='x', ascending=False)
print(decending.head(3))
```

       carat      cut color clarity  depth  table  price     x     y     z
    0   0.23    Ideal     E     SI2   61.5   55.0    326  3.95  3.98  2.43
    1   0.21  Premium     E     SI1   59.8   61.0    326  3.89  3.84  2.31
    2   0.23     Good     E     VS1   56.9   65.0    327  4.05  4.07  2.31
           carat      cut color clarity  depth  table  price    x    y    z
    49556   0.71     Good     F     SI2   64.1   60.0   2130  0.0  0.0  0.0
    26243   1.20  Premium     D    VVS1   62.1   59.0  15686  0.0  0.0  0.0
    27429   2.25  Premium     H     SI2   62.8   59.0  18034  0.0  0.0  0.0
           carat      cut color clarity  depth  table  price      x      y     z
    27415   5.01     Fair     J      I1   65.5   59.0  18018  10.74  10.54  6.98
    27630   4.50     Fair     J      I1   65.8   58.0  18531  10.23  10.16  6.72
    25998   4.01  Premium     I      I1   61.0   61.0  15223  10.14  10.10  6.17
    

# Write a Pandas program to remove the second column of the diamonds Data frame. 



```python
import pandas as pd

data = pd.read_csv("diamonds.csv")
print(data.head())
data.drop('cut', axis=1, inplace=True)
print(data.head())
```

       carat      cut color clarity  depth  table  price     x     y     z
    0   0.23    Ideal     E     SI2   61.5   55.0    326  3.95  3.98  2.43
    1   0.21  Premium     E     SI1   59.8   61.0    326  3.89  3.84  2.31
    2   0.23     Good     E     VS1   56.9   65.0    327  4.05  4.07  2.31
    3   0.29  Premium     I     VS2   62.4   58.0    334  4.20  4.23  2.63
    4   0.31     Good     J     SI2   63.3   58.0    335  4.34  4.35  2.75
       carat color clarity  depth  table  price     x     y     z
    0   0.23     E     SI2   61.5   55.0    326  3.95  3.98  2.43
    1   0.21     E     SI1   59.8   61.0    326  3.89  3.84  2.31
    2   0.23     E     VS1   56.9   65.0    327  4.05  4.07  2.31
    3   0.29     I     VS2   62.4   58.0    334  4.20  4.23  2.63
    4   0.31     J     SI2   63.3   58.0    335  4.34  4.35  2.75
    

# Write a Pandas program to find the details of the diamonds where depth>61, price>340, and cut=’Good’.


```python
import pandas as pd

data = pd.read_csv("diamonds.csv")

# Original data frame
print("Original data frame:")
print(data.head(3))

# Updated data frame
print("Updated data frame:")
data = data[(data.depth > 61) & (data.price > 340) & (data.cut == 'Good')]
print(data.head(3))
```

    Original data frame:
       carat      cut color clarity  depth  table  price     x     y     z
    0   0.23    Ideal     E     SI2   61.5   55.0    326  3.95  3.98  2.43
    1   0.21  Premium     E     SI1   59.8   61.0    326  3.89  3.84  2.31
    2   0.23     Good     E     VS1   56.9   65.0    327  4.05  4.07  2.31
    Updated data frame:
        carat   cut color clarity  depth  table  price     x     y     z
    17    0.3  Good     J     SI1   63.4    NaN    351  4.23  4.29  2.70
    18    0.3  Good     J     SI1   63.8   56.0    351  4.23  4.26  2.71
    20    0.3  Good     I     SI2   63.3   56.0    351  4.26  4.30  2.71
    

# Write a Pandas program to calculate the count, the minimum, and maximum price for each cut of diamonds Data Frame. 



```python
import pandas as pd

data = pd.read_csv("diamonds.csv")

print("Original Dataframe:")
print(data.head(3))
print("\nCount, minimum, maximum  price for each cut of diamonds DataFrame:")
print(data.groupby('cut').price.agg(['count', 'min', 'max']))
```

    Original Dataframe:
       carat      cut color clarity  depth  table  price     x     y     z
    0   0.23    Ideal     E     SI2   61.5   55.0    326  3.95  3.98  2.43
    1   0.21  Premium     E     SI1   59.8   61.0    326  3.89  3.84  2.31
    2   0.23     Good     E     VS1   56.9   65.0    327  4.05  4.07  2.31
    
    Count, minimum, maximum  price for each cut of diamonds DataFrame:
               count  min    max
    cut                         
    Fair        1610  337  18574
    Good        4906  327  18788
    Ideal      21551  326  18806
    Premium    13791  326  18823
    Very Good  12082  336  18818
    

# Write Pandas program to Demonstrate handling of Missing values (Remove column, Remove rows and Filling values Etc.)


```python
import pandas as pd

data = pd.read_csv("diamonds.csv")

# Describe Basic Information
print(data.info())
print(data.isnull().sum())
print(data.describe())
updated_data['table']=updated_data['table'].fillna(updated_data['table'].mean())
# Display after update
print(updated_data.info())
print(updated_data[7:87])
print(updated_data[updated_data['table'].isna()])
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 53940 entries, 0 to 53939
    Data columns (total 10 columns):
     #   Column   Non-Null Count  Dtype  
    ---  ------   --------------  -----  
     0   carat    53940 non-null  float64
     1   cut      53940 non-null  object 
     2   color    53940 non-null  object 
     3   clarity  53940 non-null  object 
     4   depth    53940 non-null  float64
     5   table    53939 non-null  float64
     6   price    53940 non-null  int64  
     7   x        53940 non-null  float64
     8   y        53940 non-null  float64
     9   z        53940 non-null  float64
    dtypes: float64(6), int64(1), object(3)
    memory usage: 4.1+ MB
    None
    carat      0
    cut        0
    color      0
    clarity    0
    depth      0
    table      1
    price      0
    x          0
    y          0
    z          0
    dtype: int64
                  carat         depth         table         price             x  \
    count  53940.000000  53940.000000  53939.000000  53940.000000  53940.000000   
    mean       0.797940     61.749405     57.457248   3932.799722      5.731157   
    std        0.474011      1.432621      2.234462   3989.439738      1.121761   
    min        0.200000     43.000000     43.000000    326.000000      0.000000   
    25%        0.400000     61.000000     56.000000    950.000000      4.710000   
    50%        0.700000     61.800000     57.000000   2401.000000      5.700000   
    75%        1.040000     62.500000     59.000000   5324.250000      6.540000   
    max        5.010000     79.000000     95.000000  18823.000000     10.740000   
    
                      y             z  
    count  53940.000000  53940.000000  
    mean       5.734526      3.538734  
    std        1.142135      0.705699  
    min        0.000000      0.000000  
    25%        4.720000      2.910000  
    50%        5.710000      3.530000  
    75%        6.540000      4.040000  
    max       58.900000     31.800000  
    


```python

# print Null values row
print(data[data['table'].isna()])


```

        carat   cut color clarity  depth  table  price     x     y    z
    17    0.3  Good     J     SI1   63.4    NaN    351  4.23  4.29  2.7
    


```python

# Remove rows or column
updated_data=data.dropna(axis=1)
print(updated_data)
print(updated_data.info())

```

           carat        cut color clarity  depth  price     x     y     z
    0       0.23      Ideal     E     SI2   61.5    326  3.95  3.98  2.43
    1       0.21    Premium     E     SI1   59.8    326  3.89  3.84  2.31
    2       0.23       Good     E     VS1   56.9    327  4.05  4.07  2.31
    3       0.29    Premium     I     VS2   62.4    334  4.20  4.23  2.63
    4       0.31       Good     J     SI2   63.3    335  4.34  4.35  2.75
    ...      ...        ...   ...     ...    ...    ...   ...   ...   ...
    53935   0.72      Ideal     D     SI1   60.8   2757  5.75  5.76  3.50
    53936   0.72       Good     D     SI1   63.1   2757  5.69  5.75  3.61
    53937   0.70  Very Good     D     SI1   62.8   2757  5.66  5.68  3.56
    53938   0.86    Premium     H     SI2   61.0   2757  6.15  6.12  3.74
    53939   0.75      Ideal     D     SI2   62.2   2757  5.83  5.87  3.64
    
    [53940 rows x 9 columns]
    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 53940 entries, 0 to 53939
    Data columns (total 9 columns):
     #   Column   Non-Null Count  Dtype  
    ---  ------   --------------  -----  
     0   carat    53940 non-null  float64
     1   cut      53940 non-null  object 
     2   color    53940 non-null  object 
     3   clarity  53940 non-null  object 
     4   depth    53940 non-null  float64
     5   price    53940 non-null  int64  
     6   x        53940 non-null  float64
     7   y        53940 non-null  float64
     8   z        53940 non-null  float64
    dtypes: float64(5), int64(1), object(3)
    memory usage: 3.7+ MB
    None
    


```python
# Fill missing values
updated_data = data
print(updated_data.info())


```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 53940 entries, 0 to 53939
    Data columns (total 10 columns):
     #   Column   Non-Null Count  Dtype  
    ---  ------   --------------  -----  
     0   carat    53940 non-null  float64
     1   cut      53940 non-null  object 
     2   color    53940 non-null  object 
     3   clarity  53940 non-null  object 
     4   depth    53940 non-null  float64
     5   table    53939 non-null  float64
     6   price    53940 non-null  int64  
     7   x        53940 non-null  float64
     8   y        53940 non-null  float64
     9   z        53940 non-null  float64
    dtypes: float64(6), int64(1), object(3)
    memory usage: 4.1+ MB
    None
    


```python

updated_data['table']=updated_data['table'].fillna(updated_data['table'].mean())
# Display after update
print(updated_data.info())
print(updated_data[7:87])
print(updated_data[updated_data['table'].isna()])
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 53940 entries, 0 to 53939
    Data columns (total 10 columns):
     #   Column   Non-Null Count  Dtype  
    ---  ------   --------------  -----  
     0   carat    53940 non-null  float64
     1   cut      53940 non-null  object 
     2   color    53940 non-null  object 
     3   clarity  53940 non-null  object 
     4   depth    53940 non-null  float64
     5   table    53940 non-null  float64
     6   price    53940 non-null  int64  
     7   x        53940 non-null  float64
     8   y        53940 non-null  float64
     9   z        53940 non-null  float64
    dtypes: float64(6), int64(1), object(3)
    memory usage: 4.1+ MB
    None
        carat        cut color clarity  depth  table  price     x     y     z
    7    0.26  Very Good     H     SI1   61.9   55.0    337  4.07  4.11  2.53
    8    0.22       Fair     E     VS2   65.1   61.0    337  3.87  3.78  2.49
    9    0.23  Very Good     H     VS1   59.4   61.0    338  4.00  4.05  2.39
    10   0.30       Good     J     SI1   64.0   55.0    339  4.25  4.28  2.73
    11   0.23      Ideal     J     VS1   62.8   56.0    340  3.93  3.90  2.46
    ..    ...        ...   ...     ...    ...    ...    ...   ...   ...   ...
    82   0.26      Ideal     E    VVS2   62.9   58.0    554  4.02  4.06  2.54
    83   0.38      Ideal     I     SI2   61.6   56.0    554  4.65  4.67  2.87
    84   0.26       Good     E    VVS1   57.9   60.0    554  4.22  4.25  2.45
    85   0.24    Premium     G    VVS1   62.3   59.0    554  3.95  3.92  2.45
    86   0.24    Premium     H    VVS1   61.2   58.0    554  4.01  3.96  2.44
    
    [80 rows x 10 columns]
    Empty DataFrame
    Columns: [carat, cut, color, clarity, depth, table, price, x, y, z]
    Index: []
    

# Write a program using pandas to display content of XML file. (Create any XML file of your choice) 


```python
import xml.etree.ElementTree as et

import pandas as pd

xtree = et.parse("test.xml")
xroot = xtree.getroot()

df_cols = ["name", "email", "grade", "age"]
rows = []

for node in xroot:
    s_name = node.attrib.get("name")
    s_mail = node.find("email").text if node is not None else None
    s_grade = node.find("grade").text if node is not None else None
    s_age = node.find("age").text if node is not None else None

    rows.append({"name": s_name, "email": s_mail,
                 "grade": s_grade, "age": s_age})

out_df = pd.DataFrame(rows, columns=df_cols)
print(out_df)

```

        name                    email grade age
    0  hiren  hiren14lalani@gmail.com     A  20
    1  Rajvi      rajvi@wordpress.com     B  16
    2    vur       vur@contact.hr.com     C  20
    3    tur   tur@contact.realtk.com     A  20
    

#  Write a program to demonstrate the Groupby, Join and Merge. 


```python
import pandas as pd

a = pd.DataFrame({'column1': ['A', 'C', 'D', 'E'],
                  'column2': ['F', 'G', 'H', 'I'],
                  'column3': ['J', 'K', 'L', 'M'],
                  'column4': ['N', 'O', 'P', 'Q']},
                 index=[1, 2, 3, 4])
b = pd.DataFrame({'column3': ['R', 'S', 'T', 'U'],
                  'column5': ['V', 'W', 'X', 'Y'],
                  'column6': ['Z', 'α', 'β', 'υ'],
                  'column7': ['σ', 'χ', 'ι', 'κ']},
                 index=[3, 4, 5, 6])
result = pd.concat([a, b], axis=0, join='outer')  # outer join with axis 0
print(result)
result = pd.concat([a, b], axis=1, join='outer')  # outer join with  axis=1
print(result)
result = pd.concat([a, b], axis=0, join='inner')  # inner join with axis 0
print(result)
result = pd.concat([a, b], axis=1, join='inner')  # inner join with  axis=1
print(result)

# Demonstrate Merge
c = pd.DataFrame({'key': ['A', 'C', 'D', 'E'],
                  'column2': ['F', 'G', 'H', 'I'],
                  'column3': ['J', 'K', 'L', 'M'],
                  'column4': ['N', 'O', 'P', 'Q']},
                 index=[1, 2, 3, 4])
d = pd.DataFrame({'key': ['C', 'D', 'T', 'U'],
                  'column5': ['V', 'W', 'X', 'Y'],
                  'column6': ['Z', 'α', 'β', 'υ'],
                  'column7': ['σ', 'χ', 'ι', 'κ']},
                 index=[3, 4, 5, 6])
result = pd.merge(c, d, on='key')
print(result)

# Demonstrate Groupby

e = pd.DataFrame({"key": ["a", "b", "c", "a", "b", "c"], "values": [1, 2, 3, 1, 2, 3]})
f = e.groupby("key").sum()
print(f)
```

      column1 column2 column3 column4 column5 column6 column7
    1       A       F       J       N     NaN     NaN     NaN
    2       C       G       K       O     NaN     NaN     NaN
    3       D       H       L       P     NaN     NaN     NaN
    4       E       I       M       Q     NaN     NaN     NaN
    3     NaN     NaN       R     NaN       V       Z       σ
    4     NaN     NaN       S     NaN       W       α       χ
    5     NaN     NaN       T     NaN       X       β       ι
    6     NaN     NaN       U     NaN       Y       υ       κ
      column1 column2 column3 column4 column3 column5 column6 column7
    1       A       F       J       N     NaN     NaN     NaN     NaN
    2       C       G       K       O     NaN     NaN     NaN     NaN
    3       D       H       L       P       R       V       Z       σ
    4       E       I       M       Q       S       W       α       χ
    5     NaN     NaN     NaN     NaN       T       X       β       ι
    6     NaN     NaN     NaN     NaN       U       Y       υ       κ
      column3
    1       J
    2       K
    3       L
    4       M
    3       R
    4       S
    5       T
    6       U
      column1 column2 column3 column4 column3 column5 column6 column7
    3       D       H       L       P       R       V       Z       σ
    4       E       I       M       Q       S       W       α       χ
      key column2 column3 column4 column5 column6 column7
    0   C       G       K       O       V       Z       σ
    1   D       H       L       P       W       α       χ
         values
    key        
    a         2
    b         4
    c         6
    

# Write a program to create Class Student and demonstrate the magic Function. 



```python
class student():
    def __init__(self, *args):
        print("Now called __init__ magic method, after tha initialised parameters")
        self.name = args[0]
        self.subject = args[1]
        self.marks = args[2]

    def called(self):
        print(self.name)


Student = student("hiren", "Python", 100)

print("Details are: \n", Student.name, "\n", Student.subject, "\n", Student.marks)
Student.called()


# _add_method adding two object

# Creating a class
class Method_1:
    def __init__(self, *argument):
        self.attribute = argument[0]
        self.attribute2 = argument[1]


# Creating a second class
class Method_2:
    def __init__(self, argument):
        self.attribute = argument
    # creating the instances


instance_1 = Method_1(" Arg", "Welcome")
print(instance_1.attribute)
instance_2 = Method_2("1")
print(instance_2.attribute)

# Adding two attributes of the instances
print(instance_2.attribute + instance_1.attribute)

```

    Now called __init__ magic method, after tha initialised parameters
    Details are: 
     hiren 
     Python 
     100
    hiren
     Arg
    1
    1 Arg
    

# 14. Write a program to demonstrate Bag of word model. 



```python
! pip install nltk
```


```python
import re

import nltk

# Need to install nltk using pip

# execute the text here as :
text = "Hello Everyone Hello again"

# Remove below line comment when run first time
# nltk.download('punkt')
dataset = nltk.sent_tokenize(text)
for i in range(len(dataset)):
    dataset[i] = dataset[i].lower()
    dataset[i] = re.sub(r'\W', ' ', dataset[i])
    dataset[i] = re.sub(r'\s+', ' ', dataset[i])
# Creating the Bag of Words model
word2count = {}
for data in dataset:
    words = nltk.word_tokenize(data)
    for word in words:
        if word not in word2count.keys():
            word2count[word] = 1
        else:
            word2count[word] += 1

print(word2count)
```

    {'hello': 2, 'everyone': 1, 'again': 1}
    

# TF-IDF, NLP Programming 

# 1. Write a Regular expression code to verify the email address. 



```python
import re

email = input("Enter your email address: ")
if re.match(r"^[a-zA-Z\d_.+-]+@[a-zA-Z\d]+\.[a-zA-Z\d.]+$", email):
    print("Valid email address")
else:
    print("Invalid email address")
```

    Enter your email address: hiren14lalani@gmail.com
    Valid email address
    

# Write a program to read an HTML file using the beautiful soup library and parse the
## following information.
### a. To read all the hyperlinks
### b. To real head part
### c. To real table data
### d. After reading all the information shown in a proper format 


```python
import requests
from bs4 import BeautifulSoup

html = requests.get("http://www.python.org").text
soup = BeautifulSoup(html, 'html.parser')
links = soup.find_all('a')
head = soup.find_all('head')
table = soup.find_all('table')
for i in links:
    print(i.get('href'))
for i in head:
    print(i)
for i in table:
    print(i)

```

# Write NLP program using NLTK library to read text data from website and convert into appropriate feature table using Bag of words method.


```python
import nltk
import pandas as pd
import requests
from bs4 import BeautifulSoup

html = requests.get("http://www.python.org").text
soup = BeautifulSoup(html, 'html.parser')
text = soup.get_text()

# Tokenization
tokens = [t for t in text.split()]
print(tokens)

# Frequency distribution
freq = nltk.FreqDist(tokens)
for key, val in freq.items():
    print(str(key) + ':' + str(val))

# Frequency distribution plot
freq.plot(20, cumulative=False)


# Bag of words
def bag_of_words(words):
    return dict([(word, True) for word in words])


# Get features
words = bag_of_words(tokens)
print(words)

# Data frame
df = pd.DataFrame(words.items(), columns=['words', 'count'])
print(df)
```
