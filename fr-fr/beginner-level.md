```mixed
> Recommandation: Need Exemple and Output display.
```

### is Python interpreted language? Explain
Python is an interpreted language. The Python language program runs directly from the source code. It converts the source code into an intermediate language code, which is again translated into machine language that has to be executed.

Unlike Java or C, Python does not require compilation before execution.

![Python Interview Questions](https://static.javatpoint.com/interview/images/python-interpreted-language.png)


### Give the output of this example: A[3] if A=[1,4,6,7,9,66,4,94]
Since indexing starts from zero, an element present at 3rd index is 7. 
So, the output is **7**.


### How to remove whitespaces from a string in Python?
To remove the whitespaces and trailing spaces from the string, Python providies strip([str]) built-in function. This function returns a copy of the string after removing whitespaces if present. Otherwise returns original string.
**Example:**
```python
1.  string = " javatpoint "
2.  string2 = " javatpoint "
3.  string3 = " javatpoint"
4.  print(string)
5.  print(string2)
6.  print(string3)
7.  print("After stripping all have placed in a sequence:")
8.  print(string.strip())
9.  print(string2.strip())
10.  print(string3.strip())
```
**Output:**
```console
javatpoint 
    javatpoint        
       javatpoint
After stripping all have placed in a sequence:
Javatpoint
javatpoint
javatpoint
```

### List 5 type conversion in Python

Type conversion refers to the conversion of one data type into another.

- int() - converts any data type into integer type
- float() - converts any data type into float type
- list() - This function is used to convert any data type to a list type.
- dict() - This function is used to convert a tuple of order (key,value) into a dictionary.
- str() - Used to convert integer into a string.

### What are functions in Python? Give an example & output
A function is a block of code which is executed only when a call is made to the function. **def** keyword is used to define a particular function as shown below:

**Example:**
```python
def function():
print("Hi, Welcome to Hairun Dud :)")
function(); # call to the function
```
**Output:**
```console
Hi, Welcome to Hairun Dud :)
```

### How to remove leading whitespaces from a string in the Python?
To remove leading characters from a string, we can use lstrip() function. It is Python string function which takes an optional char type parameter. If a parameter is provided, it removes the character. Otherwise, it removes all the leading spaces from the string.

**Example:**
```python
1.  string = " javatpoint "
2.  string2 = " javatpoint "
3.  print(string)
4.  print(string2)
5.  print("After stripping all leading whitespaces:")
6.  print(string.lstrip())
7.  print(string2.lstrip())
```
**Output:**
```console
javatpoint 
    javatpoint        
After stripping all leading whitespaces:
javatpoint 
javatpoint
```
### What are the common built-in data types in Python?
Python supports the below-mentioned built-in data types:

**Immutable data types:**
-   Number
-   String
-   Tuple

**Mutable data types:**
-   List
-   Dictionary
-   set


### Why do we use join() function in Python?
The join() is defined as a string method which returns a string value. It is concatenated with the elements of an iterable. It provides a flexible way to concatenate the strings. See an example below.

**Example:**
```python
1.  str = "Rohan"
2.  str2 = "ab"
3.  # Calling function
4.  str2 = str.join(str2)
5.  # Displaying result
6.  print(str2)
```
**Output:**
```console
aRohanb  
```

### What is PYTHONPATH?
**PYTHONPATH** has a role similar to PATH. This variable tells Python Interpreter where to locate the module files imported into a program. It should include the Python source library directory and the directories containing Python source code. PYTHONPATH is sometimes preset by Python Installer.


### What is a dictionary in Python?
The Python dictionary is a built-in data type. It defines a one-to-one relationship between keys and values. Dictionaries contain a pair of keys and their corresponding values. It stores elements in key and value pairs. The keys are unique whereas values can be duplicate. The key accesses the dictionary elements.

Keys index dictionaries.

**Example:**
The following example contains some keys Country Hero & Cartoon. Their corresponding values are India, Modi, and Rahul respectively.
```python
1.  dict = {'Country': 'India', 'Hero': 'Modi', 'Cartoon': 'Rahul'}
2.  print ("Country: ", dict['Country'])
3.  print ("Hero: ", dict['Hero'])
4.  print ("Cartoon: ", dict['Cartoon'])
```
**Output:**
```console
Country:  India
Hero:  Modi
Cartoon:  Rahul
```

### What does len() do?

len() is an inbuilt function used to calculate the length of sequences like list, [python string](https://intellipaat.com/blog/tutorial/python-tutorial/python-strings/), and array.

**Example:**
```python
my _list=[1,2,3,4,5]
len(my_list)
```
**Output:**
```console
5
```

### List 5 common Python Modules
Commonly used built modules are listed below:
-   os
-   sys
-   datatime
-   math
-   random

### What is the shortest method to open a text file and display its content?
The shortest way to open a text file is by using "with" command in the following manner:

**Example:**
```python
1.  with open("FILE NAME", "r") as fp:
2.  fileData = fp.read()
3.  # To print the contents of the file
4.  print(fileData)
```
**Output:**
```console
"The data of the file will be printed."
```

### Explain the use of the 'with' statement and its syntax

In Python, using the ‘with’ statement, we can open a file and close it as soon as the block of code, where ‘with’ is used, exits. In this way, we can opt for not using the close() method.

```python
with open("filename", "mode") as file_var:
```

### What does *args and **kwargs mean?

-   *args: It is used to pass multiple arguments in a function.
-   **kwargs: It is used to pass multiple keyworded arguments in a function in python.

### What is the difference between Python Arrays and lists?

Arrays and lists, in Python, have the same way of storing data. But, arrays can hold only a single data type elements whereas lists can hold any data type elements.

**Example:**
```python
1.  import array as arr
2.  User_Array = arr.array('i', [1,2,3,4])
3.  User_list = [1, 'abc', 1.20]
4.  print (User_Array)
5.  print (User_list)
```
**Output:**
```console
array('i', [1, 2, 3, 4])
[1, 'abc', 1.2]
```

### What is self in Python?

Self is an instance or an object of a class. In Python, this is explicitly included as the first parameter. However, this is not the case in Java where it's optional. It helps to differentiate between the methods and attributes of a class with local variables.

The self-variable in the init method refers to the newly created object while in other methods, it refers to the object whose method was called.


### What is __init__?
The __init__ is a method or constructor in Python. This method is automatically called to allocate memory when a new object/ instance of a class is created. All classes have the __init__ method.

**Example:**
```python
1.  class Employee_1:
2.      def __init__(self, name, age,salary):
3.          self.name = name
4.          self.age = age
5.          self.salary = 20000
6.  E_1 = Employee_1("pqr", 20, 25000)
7.  # E1 is the instance of class Employee.
8.  #__init__ allocates memory for E1.
9.  print(E_1.name)
10. print(E_1.age)
11. print(E_1.salary)
```
**Output:**
```console
pqr
20
25000
```

### What are local variables and global variables in Python?

**Local variable**: Any variable declared inside a function is known as Local variable and it’s accessibility remains inside that function only.

**Global Variable**: Any variable declared outside the function is known as Global variable and it can be easily accessible by any function present throughout the program.

**Example:**
```python
g=4   #global variable
def func_multiply():
    l=5   #local variable
    m=g*l
    return m
func_multiply()
```
**Output:** 
```console
20
```

If you try to access the local variable outside the multiply function then you will end up with getting an error.

### Write a Python program to count the total number of lines in a text file

```python
def file_count(fname):
    with open(fname) as f:
    for i, 1 in enumerate(f):
        pass
    return i+1
print(“Total number of lines in the text file: ”, file_count(“file.txt”))
```

### What would be the output if I run the following code block?

```python
list1 = [2, 33, 222, 14, 25]
print(list1[-2])
```

1.  **14**
2.  **33**
3.  **25**
4.  **Error**


**Output:**
```console
14
```
### Write a sorting algorithm for a numerical dataset in Python

```python
my_list = ["8", "4", "3", "6", "2"]
my_list = [int(i) for i in my_list]
my_list.sort()
print(my_list)
```
**Output:**
```console
[2, 3, 4, 6, 8]
```

### Write a program in Python to produce Star triangle
```python
def Star_triangle(n):
    for x in range(n):
        print(' '*(n-x-1)+'*'*(2*x+1))
Star_triangle(9)
```
**Output:**
```console
***  
*****  
*******  
*********  
***********  
*************  
***************  
*****************
```

### Write a program to produce Fibonacci series in Python
Fibonacci series refers to the series where the element is the sum of two elements prior to it.

```python
n = int(input("number of terms? "))
n1, n2 = 0, 1
count = 0
if n <= 0:
    print("Please enter a positive integer")
elif n == 1:
    print("Fibonacci sequence upto",nterms,":")
    print(n1)
else:
    print("Fibonacci sequence:")
    while count < n:
        print(n1)
        nth = n1 + n2
        n1 = n2
        n2 = nth
        count += 1
```

### Write a program in Python to check if a number is prime
```python
num = 13
if num > 1:
    for i in range(2, int(num/2)+1):
        if (num % i) == 0:
            print(num, "is not a prime number")
            break
        else:
            print(num, "is a prime number")
            break
else:
    print(num, "is not a prime number")
```

**Output:**
```console
13 is a prime number
```