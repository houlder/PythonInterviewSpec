```mixed
> Recommandation: If possible Exemple and Output display.
```
### Explain split(), sub(), subn() methods of “re” module in Python
These methods belong to the [Python RegEx or ‘re’ module](https://intellipaat.com/blog/tutorial/python-tutorial/python-regex-regular-expressions/) and are used to modify strings.

-   split(): This method is used to split a given string into a list.
-   sub(): This method is used to find a substring where a regex pattern matches, and then it replaces the matched substring with a different string.
-   subn(): This method is similar to the sub() method, but it returns the new string, along with the number of replacements.

### Write a code to display the contents of a file in reverse

To display the contents of a file in reverse, the following code can be used:

```python
for line in reversed(list(open(filename.txt))):
print(line.rstrip())
```

### Write a Python program to check whether a given string is a palindrome or not, without using an iterative method?
A palindrome is a word, phrase, or sequence that reads the same backward as forward, e.g., madam, nurses run, etc.

Consider the below code:
```python
def fun(data):
    s1 = data
    s = data[::-1]
    if(s1 == s):
        return True
    else:
        return False
print(fun('madam'))    # True
```

### Write an efficient code to count the number of capital letters in a file
The normal solution for this problem statement would be as follows:
```python
#-------------SOME_LARGE_FILE-------------
#1. HMKJlkjhmjkhmjhkjkrgerg
#2. JBHKJjklzleflklkmelkfmlskdlf
#3. KNJlk,kvz
#4. nndkslkdfjlkjfkjekj

with  open(SOME_LARGE_FILE) as countletter:
    count =  0
    text = countletter.read()
    for character in text:
        if character.isupper():
            count +=  1
    print(count)
```
To make this code more efficient, the whole code block can be converted into a one-liner code using the feature called generator expression. 
With this, the equivalent code line of the above code block would be as follows:
```python
#-------------countletter-------------
#1. HMKJlkjhmjkhmjhkjkrgerg
#2. JBHKJjklzleflklkmelkfmlskdlf
#3. KNJlk,kvz
#4. nndkslkdfjlkjfkjekj

count = sum(1 for line in countletter for character in line if character.isupper())
print(count)

**Output**
```console
12
```

### Demonstrate how to send an email in Python Language using smtplib

To send an email, Python provides smtplib and email modules. Import these modules into the created mail script and send mail by authenticating a user.

It has a method SMTP(smtp-server, port). It requires two parameters to establish SMTP connection.

A simple example to send an email is given below.

**Example:**
```python
1.  import smtplib
2.  # Calling SMTP
3.  s = smtplib.SMTP('smtp.gmail.com', 587)
4.  # TLS for network security
5.  s.starttls()
6.  # User email Authentication
7.  s.login("sender@email_id", "sender_email_id_password")
8.  # Message to be sent
9.  message = "Message_sender_need_to_send"
10.  # Sending the mail
11.  s.sendmail("sender@email_id ", "receiver@email_id", message)
```

### What are Dict and List comprehensions?

[Python comprehensions](https://intellipaat.com/blog/tutorial/python-tutorial/python-list-comprehension/) are like decorators, that help to build altered and filtered lists, dictionaries, or sets from a given list, dictionary, or set. Comprehension saves a lot of time and code that might be considerably more complex and time-consuming.

Comprehensions are beneficial in the following scenarios:

-   Performing mathematical operations on the entire list
-   Performing conditional filtering operations on the entire list
-   Combining multiple lists into one
-   Flattening a multi-dimensional list

**Example 1**
```python
my_list = [2, 3, 5, 7, 11]
squared_list = [x**2 for x in my_list]    # list comprehension
```
**Output:**
```console
[4 , 9 , 25 , 49 , 121]
```
**Example 2**
```python
squared_dict = {x:x**2 for x in my_list}    # dict comprehension
```
**Output:**
```console
{11: 121, 2: 4 , 3: 9 , 5: 25 , 7: 49}
```

### What is pandas?

Pandas is an open source python library which supports data structures for data based operations associated with data analyzing and data Manipulation . Pandas with its rich sets of features fits in every role of data operation,whether it be related to implementing different algorithms or for solving complex business problems. Pandas helps to deal with a number of files in performing certain operations on the data stored by files.

### Why would you use NumPy arrays instead of lists in Python?

NumPy arrays provide users with three main advantages as shown below:

- NumPy arrays consume a lot less memory, thereby making the code more efficient.
- NumPy arrays execute faster and do not add heavy processing to the runtime.
- NumPy has a highly readable syntax, making it easy and convenient for programmers.

### How do you identify missing values and deal with missing values in Dataframe?

**Identification**:
isnull() and isna() functions are used to identify the missing values in your data loaded into dataframe.
```python
missing_count=data_frame1.isnull().sum()
```
**Handling missing Values**:
There are two ways of handling the missing values :
Replace the missing values with 0
```python
df[‘col_name’].fillna(0)
```
Replace the missing values with the mean value of that column.
```python
df[‘col_name’] = df[‘col_name’].fillna((df[‘col_name’].mean()))
```

### Can you give me an example of how to use HTTP methods with routes in FastAPI?
You can use HTTP methods with routes in FastAPI by specifying the methods argument with a list of methods when you add a route. For example, if you want to add a route that can be accessed with the GET and POST methods, you would do the following:

  ```python
@app.get(“/my-route”, methods=[“GET”, “POST”])
def my_route():
return “Hello, world!”
  ```

### What are some common error codes returned by FastAPI?
Some common error codes that may be returned by FastAPI include:

- 400: Bad Request
- 401: Unauthorized
- 403: Forbidden 
- 404: Not Found
- 405: Method Not Allowed
- 500: Internal Server Error


### What is the best way to test endpoints that have been created using FastAPI?
There are a few different ways to test endpoints created with FastAPI. One way is to use the built-in test client that is provided. Another way is to use a tool like Postman.


### Can I upload files in FastAPI? If yes, then how?
Yes, you can upload files in FastAPI. There are a few different ways to do it, but the most common way is to use the FileUpload class. This class allows you to specify the maximum file size, the allowed file types, and the storage location for the uploaded files.


### What is UTF8JSONResponse?
UTF8JSONResponse is a class used in FastAPI to return responses that are encoded in UTF-8 and formatted as JSON. This is useful for APIs that need to support international characters, as UTF-8 is a widely used encoding that can represent most languages.

### Explain the use of session in Django framework

Django provides a session that lets the user store and retrieve data on a per-site-visitor basis. Django abstracts the process of sending and receiving cookies, by placing a session ID cookie on the client side, and storing all the related data on the server side.

![Python Interview Questions](https://static.javatpoint.com/interview/images/python-interview-q58.png)

So, the data itself is not stored client side. This is good from a security perspective.

### How does Python Flask handle database requests?

Flask supports a database-powered application (RDBS). Such a system requires creating a schema, which needs piping the schema.sql file into the sqlite3 command. Python developers need to install the sqlite3 command to create or initiate the database in Flask.

Flask allows to request for a database in three ways:

-   before_request(): They are called before a request and pass no arguments.
-   after_request(): They are called after a request and pass the response that will be sent to the client.
-   teardown_request(): They are called in a situation when an exception is raised and responses are not guaranteed. They are called after the response has been constructed. They are not allowed to modify the request, and their values are ignored.

