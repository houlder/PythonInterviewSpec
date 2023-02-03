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

### Can you explain the architecture of FastAPI?

FastAPI is built on top of Starlette, which is a lightweight ASGI framework. FastAPI then adds additional features on top of Starlette, such as automatic data validation, serialization, and documentation.

### How do you define a route in FastAPI?

In FastAPI, routes are defined using decorators. For example, to define a route that returns a list of users, you would use the @get decorator:

```python
@get(“/users”)  
def list_users():  
return [{“username”: “jane”}, {“username”: “joe”}]
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

### What are some advantages of using FastAPI over Flask?

FastAPI is built on top of Starlette, which is a lightweight ASGI framework. This makes it ideal for building high-performance web applications. Additionally, FastAPI comes with built-in support for data validation, authentication, and documentation.

### What is UTF8JSONResponse?
UTF8JSONResponse is a class used in FastAPI to return responses that are encoded in UTF-8 and formatted as JSON. This is useful for APIs that need to support international characters, as UTF-8 is a widely used encoding that can represent most languages.

### What is uvicorn? Why should it be used with FastAPI?

Uvicorn is a web server that is specifically designed for use with the FastAPI web framework. It is built on top of the asyncio library and provides a very fast and efficient way to serve web applications.

#### What are OpenAPI specifications and why are they important?

OpenAPI specifications are important because they provide a standard, language-agnostic way of describing REST APIs. This allows developers to more easily understand how an API works, and also allows for tools to be built that can automatically generate code or documentation based on the OpenAPI specification.

### Do clients need to support JSON schema or OpenAPI specifications to interact with your API?

No, clients do not need to support JSON schema or OpenAPI specifications to interact with your API. However, doing so would certainly make things easier, as it would allow them to automatically generate code to interact with your API.

### What are Django-admin and manage.py and explain their commands?

“Django-admin” is the command line utility of Django to perform administrative tasks. And manage.py is created automatically in every Django project. It performs the same functions as Django-admin, but it also modifies the DJANGO SETTINGS MODULE environment variable to point to your project's settings.py file.

### Explain the use of session in Django framework

Django provides a session that lets the user store and retrieve data on a per-site-visitor basis. Django abstracts the process of sending and receiving cookies, by placing a session ID cookie on the client side, and storing all the related data on the server side.

![Python Interview Questions](https://static.javatpoint.com/interview/images/python-interview-q58.png)

So, the data itself is not stored client side. This is good from a security perspective.

### In Django’s context, what’s the difference between a project and an app?

The project covers the entire application, while an app is a module or application within the project that deals with one dedicated requirement. So, a project consists of several apps, while an app features in multiple projects.

### Discuss Django’s Request/Response Cycle.

Starting the process off, the Django server receives a request. The server then looks for a matching URL in the URL patterns defined for the project. If the server can’t find a matching URL, it produces a 404-status code. If the URL matches, it executes the corresponding code in the view file associated with the URL and sends a response.

### What are Django.shortcuts.render functions?

The render function is a shortcut function that allows the developer to quickly pass the data dictionary together with the template. The template is then combined with the data dictionary using the templating engine in this function. Finally, the render() function provides a HttpResponse containing the rendered text, which is the data returned by the models. As a result, Django render() saves the developer time and allows him to utilize multiple template engines.

### What is the Django Rest Framework?

The Django Rest Framework (DRF) is a framework that helps you quickly create RESTful APIs. They are ideal for web applications due to low bandwidth utilization.

### What do you use middleware for in Django?
You use middleware for four different functions:
-   Content Gzipping
-   Cross-site request forgery protection
-   Session management
-   Use authentication

### How can you see raw SQL queries running in Django?
To begin, make sure that the DEBUG setting is set to True. If the setting is squared away, then type the following commands:

1) from Django.db import connection
2) connection.queries

### List several caching strategies supported by Django
Django supports these caching strategies:
-   Database caching
-   In-memory caching
-   File System Caching
-   Memcached

### What is a QuerySet in the context of Django?
QuerySet is a collection of SQL queries. The command print(b.query) shows you the SQL query created from the Django filter call.

### Difference between Django OneToOneField and ForeignKey Field?

Both are among the most frequent sorts of fields in Django. 
The sole difference between these two is that the ForeignKey field includes an on_delete option in addition to a model's class because it is used for many-to-one relationships, whilst the OneToOneField only handles one-to-one relationships and requires only the model's class.

### How to combine multiple QuerySets in a View?

QuerySets can be combined into another QuerySet, and they do not have to be from the same model.
To merge QuerySets from the same model, use the Python union operator.
The union operator can be used to combine two or more QuerySets with the following syntax:
```python
model_combination = model_set1 | model_set2 | model_set3
```
Additionally, you can concatenate two or more QuerySets from other models by using the chain() method from the Itertools package.
```python
from itertools import chain
model_combination = list(chain(model_set1, model_set2))
```
As an alternative, you can merge two or more QuerySets from other models using union(), passing all=TRUE to allow for duplication.
```python
model_combination = model_set1.union(model_set2, all=TRUE)
```
### Difference between select_related and prefetch_related?
Django's select-related and prefetch-related functions are intended to reduce the number of database queries that are generated when related objects are accessed.

When a query is executed, select related() "follows" foreign-key relationships and choose extra related-object data.

Prefetch related() performs the "joining" in Python by performing a separate lookup for each relationship.

When picking a single object, such as an OneToOneField or a ForeignKey, users utilize the select-related function. When retrieving a "set" of items, such as ManyToManyFields or reverse ForeignKeys, users utilize prefetch related.

### Explain Q objects in Django ORM
When writing complex queries, Q objects are employed because filter() functions only allow you to 'AND' the conditions; whereas, Q objects allow you to 'OR' the conditions.

### What are Django exceptions?
An exception is an unusual event that causes a programme to fail. Django has its exception classes to cope with this circumstance, and it also supports all fundamental Python exceptions. The Django. core. exceptions module defines the Django core exceptions classes.

### Name the types of applications developers can create using Flask

There are plenty of applications developers can create using Flask. Your applicants should be able to name at least three. Some examples of Flask web applications include:

-   SAS apps
-   Static sites
-   Serverless applications
-   Single-page apps
-   Medium-sized websites
-   RESTful API apps

### Is the Flask framework open-source?

If your developers have general knowledge of the Flask framework, they should know that it’s open-source. They may also add that Flask is a Python-based framework.

### Can you explain why Flask is referred to as a micro-framework?

Since the Flask framework offers core features only, including blueprints and request routing, it is known as a micro-framework. Knowledgeable candidates will also know that Flask extensions allow developers to use other features like forms and caching.

### What does the /s, /b, /n  PDB command do?
- /s
To test your candidates’ technical knowledge, ask them this Flask interview question. Your applicants should know that the /s PDB command is a function that will debug an application in Flask step by step.
- /b
Knowledgeable applicants will know that the /b PDB command will create breakpoints in a program’s execution when a developer has specified particular parameters.
- /n
Candidates should be aware that the /n PDB command will continue execution up until the program reaches the next line of the current function.

### Describe what the PUT, DELETE method does in Flask
- PUT
Applicants who understand the Flask framework will know that the PUT method will replace current data corresponding to target resources with uploaded content.
- DELETE
Candidates who have top technical Flask framework knowledge will be able to explain that the DELETE method will remove the target resources’ current representations suggested by a URL.

### How does Python Flask handle database requests?

Flask supports a database-powered application (RDBS). Such a system requires creating a schema, which needs piping the schema.sql file into the sqlite3 command. Python developers need to install the sqlite3 command to create or initiate the database in Flask.

Flask allows to request for a database in three ways:

-   before_request(): They are called before a request and pass no arguments.
-   after_request(): They are called after a request and pass the response that will be sent to the client.
-   teardown_request(): They are called in a situation when an exception is raised and responses are not guaranteed. They are called after the response has been constructed. They are not allowed to modify the request, and their values are ignored.

### Explain how to add the mailing feature in the Flask Application
To send emails, we need to install the Flask-Mail flask extension using the below-given command.
```python
pip install Flask-Mail
```

Once installed, then we need to use Flask Config API to configure:
- MAIL-SERVER
-  MAIL_PORT
- MAIL_USERNAME
- MAIL_PASSWORD, etc.

Then we need to import Message Class, instantiate it and form a message object before sending the email by using the mail.send() method.

**Example:**
```python
from flask_mail import Mail, Message
from flask import Flask
app = Flask(__name__)
mail = Mail(app)
@app.route(“/mail”)
def email():
msg = Message( “Hello Message”, sender=”admin@test.com”, recipients=[“to@test.com”])
mail.send(msg)
```

### How to change default host and port in Flask?
Flask default host and port can be changed by passing the values to host and port parameters while calling run method on the app.
```python
from flask import Flask
app = Flask(__name__)
@app.route("/")
def index():
    return "Hello, World!"
if __name__=="__main__":
    app.run(host="0.0.0.0", port=8080)
```
