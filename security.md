# Security


### Explain what is web session?
Web session, the session is a data structure that an application uses to store temporary data that is useful only during the time a user is interacting with the application.
It may store in cookie, file or DB.

### Describe cross-site request forgery, cross-site scripting, session hijacking, and session fixation attacks.
- Cross-site request forgery, also known as one-click attack or session riding and abbreviated as CSRF  or XSRF, is a type of malicious exploit of a website where unauthorized commands are transmitted from a user that the web application trusts.There are many ways in which a malicious website can transmit such commands; specially-crafted image tags, hidden forms, and JavaScript XMLHttpRequests, for example, can all work without the user's interaction or even knowledge.

- Cross-site scripting -  type of computer security vulnerability typically found in web applications. 
XSS enables attackers to inject client-side scripts into web pages viewed by other users. A cross-site scripting vulnerability may be used by attackers to bypass access controls such as the same-origin policy.

- Session Hijacking attack consists of the exploitation of the web session control mechanism, which is normally managed for a session token.

- The Session Hijacking attack compromises the session token by stealing or predicting a valid session token to gain unauthorized access to the Web Server.

- Session Fixation is an attack that permits an attacker to hijack a valid user session. The attack explores a limitation in the way the web application manages the session ID, more specifically the vulnerable web application. 
When authenticating a user, it doesn’t assign a new session ID, making it possible to use an existent session ID.

### What is SQL Injection?
SQL injection is a code injection technique that might destroy your database.
```
params[:name] = "') OR 1--"
User.where("name = '#{params[:name]}'").first
```
That will changed to 
```
This will run: SELECT "users".* FROM "users" WHERE (name = '') OR 1--') LIMIT 1
```

### How should you store secure data such as a password?
Passwords and secret keys are usually stored in their hashed form. That means they are processed through a hash function before being saved to the database. A good hash function such as bcrypt has the following properties:

- it produces the same output for the same input
- it produces very different output for different inputs
- its output is not distinguishable from random
- it is not reversible

### Why do we need to use HTTPS instead of HTTP?
Http is just an application layer protocol that uses tcp to communicate on port 80. Whenever you go about searching any website this is the protocol used by default. Http is used for data transfer over the net but it is not secure. Anybody who knows how to intercept it can intercept it easily.

Now people couldn’t have that now could they? Your precious credit card information being stolen in between the transfer. That is when https came into play. Https uses cryptographic protocols like ssl encryption to secure that data.

### Explain mass-assignment vulnerability.
In order to reduce the work for developers, many frameworks provide convenient mass-assignment functionality. This lets developers inject an entire set of user-entered data from a form directly into an object or database. Without it, developers would be forced to tediously add code specifically for each field of data, cluttering the code base with repeated form mapping code.

The downside of this functionality is that it is often implemented without a whitelist that prevents users from assigning data to protected fields. An attacker may exploit this vulnerability to gain access to sensitive data or to cause data loss.

For example
```
<form method="post" action="/signup">
  <!-- INJECTED FIELD: -->
  <input type="hidden" name="is_administrator" value="true">

  <p>
    Enter your email address:
    <input type="text" name="user[email]">
  </p>
  <p>
    Select a password:
    <input type="password" name="user[password]">
  </p>

  <input type="submit" value="Sign up">
</form>
```

The controller action will create the user, letting the attacker gain complete control of the web shop:

```
def signup
  @user = User.create(params[:user])
  # => User<email: "john@doe.com", password: "qwerty", is_administrator: true>
end
```

### Explain difference between Symmetric-key and  asymmetric cryptography(Public) algorithm.
- TODO:answear