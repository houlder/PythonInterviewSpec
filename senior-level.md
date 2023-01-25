```mixed
> Recommandation: If possible Exemple and Output display.
```
### Explain split(), sub(), subn() methods of “re” module in Python
These methods belong to the [Python RegEx or ‘re’ module](https://intellipaat.com/blog/tutorial/python-tutorial/python-regex-regular-expressions/) and are used to modify strings.

-   split(): This method is used to split a given string into a list.
-   sub(): This method is used to find a substring where a regex pattern matches, and then it replaces the matched substring with a different string.
-   subn(): This method is similar to the sub() method, but it returns the new string, along with the number of replacements.

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
12. ```


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