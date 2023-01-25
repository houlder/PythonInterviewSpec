```mixed
> Recommandation: Need Exemple and Output display.
```
### Give an example of shuffle() method?
This method shuffles the given string or an array. It randomizes the items in the array. This method is present in the random module. So, we need to import it and then we can call the function. It shuffles elements each time when the function calls and produces different output.

**Example:**
```python
1.  # import the random module
2.  import random
3.  # declare a list
4.  sample_list1 = ['Z', 'Y', 'X', 'W', 'V', 'U']
5.  print("Original LIST1: ")
6.  print(sample_list1)
7.  # first shuffle
8.  random.shuffle(sample_list1)
9.  print("\nAfter the first shuffle of LIST1: ")
10.  print(sample_list1)
11.  # second shuffle
12.  random.shuffle(sample_list1)
13.  print("\nAfter the second shuffle of LIST1: ")
14.  print(sample_list1)
```
**Output:**
```console
Original LIST1: 
['Z', 'Y', 'X', 'W', 'V', 'U']

After the first shuffle of LIST1: 
['V', 'U', 'W', 'X', 'Y', 'Z']

After the second shuffle of LIST1: 
['Z', 'Y', 'X', 'U', 'V', 'W']
```

### List 11 type conversion in Python

Type conversion refers to the conversion of one data type into another.

- int() - converts any data type into integer type
- float() - converts any data type into float type
- ord() - converts characters into integer
- hex() - converts integers to hexadecimal
- oct() - converts integer to octal
- tuple() - This function is used to convert to a tuple.
- set() - This function returns the type after converting to set.
- list() - This function is used to convert any data type to a list type.
- dict() - This function is used to convert a tuple of order (key,value) into a dictionary.
- str() - Used to convert integer into a string.
- complex(real,imag) - This functionconverts real numbers to complex(real,imag) number.

### What is the use of break statement?
The break statement is used to terminate the execution of the current loop. Break always breaks the current execution and transfer control to outside the current block. If the block is in a loop, it exits from the loop, and if the break is in a nested loop, it exits from the innermost loop.
**Example:**
```python
1.  list_1 = ['X', 'Y', 'Z']
2.  list_2 = [11, 22, 33]
3.  for i in list_1:
4.      for j in list_2:
5.          print(i, j)
6.      if i == 'Y' and j == 33:
7.          print('BREAK')
8.          break
9.      else:
10.        continue
11.        break
```
**Output:**
```console
X 11
X 22
X 33
Y 11
Y 22
Y 33
BREAK
```

### How to create a Unicode string in Python?
In Python 3, the old Unicode type has replaced by "str" type, and the string is treated as Unicode by default. We can make a string in Unicode by using art.title.encode("utf-8") function.

**Example:**
```python
1.  unicode_1 = ("\u0123", "\u2665", "\U0001f638", "\u265E", "\u265F", "\u2168")
2.  print (unicode_1)

1.  unicode_1 = ("\u0123", "\u2665", "\U0001f638", "\u265E", "\u265F", "\u2168")
2.  print (unicode_1)
```
**Output:**
```console
unicode_1: ('ģ', '♥', '😸', '♞', '♟', 'Ⅸ')
```

### What is pep 8?
PEP in Python stands for Python Enhancement Proposal. It is a set of rules that specify how to write and design Python code for maximum readability.

### What is the lambda function in Python?
A lambda function is an anonymous function (a function that does not have a name) in Python. To define anonymous functions, we use the ‘lambda’ keyword instead of the ‘def’ keyword, hence the name ‘lambda function’. Lambda functions can have any number of arguments but only one statement.

**Example:**
```python
l = lambda x,y : x*y
print(a(5, 6))
```
**Output:**
```console
30
```

### What is slicing in Python?
Slicing is a mechanism used to select a range of items from sequence type like list, tuple, and string. It is beneficial and easy to get elements from a range by using slice way. It requires a : (colon) which separates the start and end index of the field. All the data collection types List or tuple allows us to use slicing to fetch elements. Although we can get elements by specifying an index, we get only single element whereas using slicing we can get a group of elements.

![Python Interview Questions](https://static.javatpoint.com/interview/images/slicing-in-python.png)

**Example:**
```python
1.  Q = "JavaTpoint, Python Interview Questions!"
2.  print(Q[2:25])
```
**Output:**
```console
vaTpoint, Python Interv
```

### Explain docstring in Python
The Python docstring is a string literal that occurs as the first statement in a module, function, class, or method definition. It provides a convenient way to associate the documentation.
- String literals occurring immediately after a simple assignment at the top are called "attribute docstrings".
- String literals occurring immediately after another docstring are called "additional docstrings".
- Python uses triple quotes to create docstrings even though the string fits on one line.

Docstring phrase ends with a period (.) and can be multiple lines. It may consist of spaces and other special chars.

**Example:**
```python
1.  # One-line docstrings
2.  def hello():
3.  """A function to greet."""
4.  return  "hello"
```

### What is the usage of help() and dir() function in Python?
Help() and dir() both functions are accessible from the Python interpreter and used for viewing a consolidated dump of built-in functions.

**Help() function**: The help() function is used to display the documentation string and also facilitates us to see the help related to modules, keywords, and attributes.

**Dir() function**: The dir() function is used to display the defined symbols.


### What are the differences between Python 2.x and Python 3.x?
Python 2.x is an older version of Python. Python 3.x is newer and latest version. Python 2.x is legacy now. Python 3.x is the present and future of this language.

The most visible difference between Python2 and Python3 is in print statement (function). 
- In Python 2, it looks like print "Hello"
- In Python 3, it is print ("Hello").

String in Python2 is ASCII implicitly, and in Python3 it is Unicode.

The xrange() method has removed from Python 3 version. A new keyword as is introduced in Error handling.

### What is the usage of enumerate() function in Python?
The enumerate() function is used to iterate through the sequence and retrieve the index position and its corresponding value at the same time.

**Example:**
```python
1.  list_1 = ["A","B","C"]
2.  s_1 = "Javatpoint"
3.  # creating enumerate objects
4.  object_1 = enumerate(list_1)
5.  object_2 = enumerate(s_1)

7.  print ("Return type:",type(object_1))
8.  print (list(enumerate(list_1)))
9.  print (list(enumerate(s_1)))
```

**Output:**
```console
Return type:
[(0, 'A'), (1, 'B'), (2, 'C')]
[(0, 'J'), (1, 'a'), (2, 'v'), (3, 'a'), (4, 't'), (5, 'p'), (6, 'o'), (7, 'i'), (8, 'n'), (9, 't')]
```

### What does [::-1] do?
[::-1] ,this is an example of slice notation and helps to reverse the sequence with the help of indexing.
**[Start,stop,step count]**

**Example:**
```python
import array as arr
Array_d=arr.array('i',[1,2,3,4,5])
Array_d[::-1]    #reverse the array or sequence
```
**Output:** 
```console
5,4,3,2,1
```

### What is a map function in Python? Put 3 different example of using it.
The map() function in Python has two parameters, function and iterable. The map() function takes a function as an argument and then applies that function to all the elements of an iterable, passed to it as another argument. It returns an object list of results.

**Example 1**
```python
def addition(n):
    return n + n
# We double all numbers using map()
numbers = (1, 2, 3, 4)
result = map(addition, numbers)
print(list(result))
```
**Output:**
```console
[2, 4, 6, 8]
```
**Example 2**
```python
# Double all numbers using map and lambda
numbers = (1, 2, 3, 4)
result = map(lambda x: x + x, numbers)
print(list(result))
```
**Output:**
```console
[2, 4, 6, 8]
```
**Example 3**
```python
# Add two lists using map and lambda
numbers1 = [1, 2, 3]
numbers2 = [4, 5, 6]
result = map(lambda x, y: x + y, numbers1, numbers2)
print(list(result))
```
**Output:**
```console
[5, 7, 9]
```

### How can the ternary operators be used in python?

The ternary operator is the operator that is used to show [conditional statements in Python](https://intellipaat.com/blog/tutorial/python-tutorial/python-if-else-statements/). This consists of the boolean true or false values with a statement that has to be checked.

**Syntax:**
```python
[on_true] if [expression] else [on_false]x, y = 10, 20 count = x if x < y else y
```
**Explanation:**

The above expression is evaluated like if x < y else y, in this case, if x < y is true then the value is returned as count = x and if it is incorrect then count = y will be stored to result.

### How will you remove duplicate elements from a list?

To remove duplicate elements from the list we use the set() function.

**Example:**
```python
demo_list=[5,4,4,6,8,12,12,1,5]
print(demo_list)
unique_list = list(set(demo_list))
print(unique_list)
```
**Output:**
```console
[5,4,4,6,8,12,12,1,5]
[1,5,6,8,12]
```

### How can files be deleted in Python?

You need to import the OS Module and use os.remove() function for deleting a file in python.  

```python
import os
os.remove("file_name.txt")
```
### Write a program in Python to execute the Bubble sort algorithm

```python
def bubbleSort(x):
    n = len(x)
    # Traverse through all array elements
    for i in range(n-1):
        for j in range(0, n-i-1):
            if x[j] > x[j+1] :
                x[j], x[j+1] = x[j+1], x[j]
# Driver code to test above
arr = [25, 34, 47, 21, 22, 11, 37]
bubbleSort(arr)
print ("Sorted array is:")
print(arr)
```

**Output:**
```console
Sorted array is:
[11, 21, 22, 25, 34, 37, 47]
```

###  Write a Program to print ASCII Value of a character in python
```python
x= 'a'
# print the ASCII value of assigned character stored in x
print(" ASCII value of '" + x + "' is", ord(x))
```
**Output:**
```console
ASCII value of 'a' is 97
```