# Javascript

### Explain how ajax works, hitting all parts of the stack.

1. User sends a request from the UI and a javascript call goes to XMLHttpRequest object.
2. HTTP Request is sent to the server by XMLHttpRequest object.
3. Server interacts with the database using JSP, PHP, Servlet, ASP.net etc.
4. Data is retrieved.
5. Server sends XML data or JSON data to the XMLHttpRequest callback function.
6. HTML and CSS data is displayed on the browser.

### How how each of these functions works - apply, call, bind.

call() - function a
With the apply() method, you can write a method that can be used on different objects.

apply() - is similar to the call() method (previous chapter) use with array with arguments.

The first parameter to the bind() method sets the value of "this" in the target function when the bound function is called. Please note that the value for first parameter is ignored if the bound function is constructed using the "new" operator.

bind() -  method are passed as arguments which are prepended to the arguments provided to the bound function when invoking the target function.

