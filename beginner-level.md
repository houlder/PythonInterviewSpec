```mixed
> Recommandation: Need Exemple and Output display.
```

### is Python interpreted language? Explain
Python is an interpreted language. The Python language program runs directly from the source code. It converts the source code into an intermediate language code, which is again translated into machine language that has to be executed.

Unlike Java or C, Python does not require compilation before execution.

![Python Interview Questions](https://static.javatpoint.com/interview/images/python-interpreted-language.png)


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

### What are functions in Python?
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