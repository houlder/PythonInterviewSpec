```mixed
> Recommandation: If possible Exemple and Output display.
```

#### Can you give me an example of how to use HTTP methods with routes in FastAPI?
You can use HTTP methods with routes in FastAPI by specifying the methods argument with a list of methods when you add a route. For example, if you want to add a route that can be accessed with the GET and POST methods, you would do the following:

  ```python
@app.get(“/my-route”, methods=[“GET”, “POST”])
def my_route():
return “Hello, world!”
  ```

### What are some common error codes returned by FastAPI?
Some common error codes that may be returned by FastAPI include:

-400: Bad Request
-401: Unauthorized
-403: Forbidden 
-404: Not Found
-405: Method Not Allowed
-500: Internal Server Error


### What is the best way to test endpoints that have been created using FastAPI?
There are a few different ways to test endpoints created with FastAPI. One way is to use the built-in test client that is provided. Another way is to use a tool like Postman.


### Can I upload files in FastAPI? If yes, then how?
Yes, you can upload files in FastAPI. There are a few different ways to do it, but the most common way is to use the FileUpload class. This class allows you to specify the maximum file size, the allowed file types, and the storage location for the uploaded files.


### What is UTF8JSONResponse?
UTF8JSONResponse is a class used in FastAPI to return responses that are encoded in UTF-8 and formatted as JSON. This is useful for APIs that need to support international characters, as UTF-8 is a widely used encoding that can represent most languages.