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
### What is the use of break statement?
The break statement is used to terminate the execution of the current loop. Break always breaks the current execution and transfer control to outside the current block. If the block is in a loop, it exits from the loop, and if the break is in a nested loop, it exits from the innermost loop.
**Example:**
```python
1.  list_1 = ['X', 'Y', 'Z']
2.  list_2 = [11, 22, 33]
3.  for i in list_1:
4.      for j in list_2:
5.          print(i, j)
6.          if i == 'Y' and j == 33:
7.              print('BREAK')
8.              break
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
String literals occurring immediately after a simple assignment at the top are called "attribute docstrings".
String literals occurring immediately after another docstring are called "additional docstrings".
Python uses triple quotes to create docstrings even though the string fits on one line.
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