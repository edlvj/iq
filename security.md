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
https://www.owasp.org/index.php/Session_fixation

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
- TODO:answear

### Why do we need to use HTTPS instead of HTTP?
- TODO:answear

### Explain mass-assignment vulnerability.
- TODO:answear

### Explain difference between Symmetric-key and  asymmetric cryptography(Public) algorithm.
- TODO:answear