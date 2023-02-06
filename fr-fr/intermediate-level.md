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

### Comment créer une chaîne Unicode en Python ?

Dans Python 3, l'ancien type Unicode a été remplacé par le type "str", et la chaîne est traitée en Unicode par défaut. Nous pouvons rendre une chaîne en Unicode en utilisant la fonction art.title.encode("utf-8").

**Exemple:**
```python
    unicode_1 = ("\u0123", "\u2665", "\U0001f638", "\u265E", "\u265F", "\u2168")
    print(unicode_1)
```
**Sortie:**
```console
    unicode_1 : ('ģ', '♥', '😸', '♞', '♟', 'Ⅸ')
```

### What is pep 8?
PEP in Python stands for Python Enhancement Proposal. It is a set of rules that specify how to write and design Python code for maximum readability.

### What is the lambda function in Python?
A lambda function is an anonymous function (a function that does not have a name) in Python. To define anonymous functions, we use the ‘lambda’ keyword instead of the ‘def’ keyword, hence the name ‘lambda function’. Lambda functions can have any number of arguments but only one statement.

**Example:**
```python
a = lambda x,y : x*y
print(a(5, 6))
```
**Output:**
```console
30
```

### Qu'est-ce que le slicing en Python ?

Le **slicing** ou découpage en tranches est un mécanisme utilisé pour sélectionner une gamme d'éléments à partir d'une séquence de type liste, tuple et chaîne. Il est avantageux et facile d'obtenir des éléments d'une plage en utilisant la méthode de découpage. 
Elle nécessite un ***:*** (deux points) qui sépare l'indice de début et de fin du champ.
Tous les types de collecte de données (liste ou tuple) nous permettent d'utiliser le découpage pour récupérer des éléments. Bien que nous puissions obtenir des éléments en spécifiant un index, nous n'obtenons qu'un seul élément alors qu'en utilisant le slicing nous pouvons obtenir un groupe d'éléments.

![Questions d'entretien sur Python](https://static.javatpoint.com/interview/images/slicing-in-python.png)

**Exemple:**
```python
    1.  Q = "JavaTpoint, Python Interview Questions !"
    2. print(Q[2:25])
```
**Sortie:**
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


### Quelles sont les différences entre Python 2.x et Python 3.x ?

Python 2.x est une ancienne version de Python. Python 3.x est une version plus récente. Python 2.x est l'héritage actuel. Python 3.x est le présent et l'avenir de ce langage.

La différence la plus visible entre Python 2 et Python 3 est l'instruction print (fonction). 
- En Python 2, cela ressemble à print "Hello".
- En Python 3, c'est print ("Hello").

La chaîne de caractères dans Python2 est implicitement ASCII, et dans Python3 elle est Unicode.

La méthode xrange() a été supprimée de la version Python 3. Un nouveau mot-clé as est introduit dans Error handling.

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

### Qu'est-ce qu'une fonction map en Python ? Donnez 3 exemple différent d'utilisation

La fonction map() en Python a deux paramètres, function et iterable. La fonction map() prend une fonction en argument, puis applique cette fonction à tous les éléments d'un itérable, qui lui est passé comme autre argument. Elle renvoie une liste d'objets de résultats.

**Exemple 1**
```python
    def addition(n) :
        return n + n
    # Nous doublons tous les nombres en utilisant map()
    nombres = (1, 2, 3, 4)
    résultat = map(addition, nombres)
    print(liste(résultat))
```
**Sortie:**
```console
    [2, 4, 6, 8]
```
**Exemple 2**
```python
    # Doublez tous les nombres en utilisant map et lambda
    nombres = (1, 2, 3, 4)
    résultat = map(lambda x : x + x, nombres)
    print(liste(résultat))
```
**Sortie:**
```console
    [2, 4, 6, 8]
```
**Exemple 3**
```python
    # Ajoutez deux listes en utilisant map et lambda
    nombres1 = [1, 2, 3]
    nombres2 = [4, 5, 6]
    result = map(lambda x, y : x + y, nombres1, nombres2)
    print(liste(résultat))
```
**Sortie:**
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