# Ruby on Rails

### What is Rack?
Rack provides a minimal interface between webservers that support Ruby and Ruby frameworks.

### Explain the Rack application interface.
To use Rack, provide an "app": an object that responds to the call method, taking the environment hash as a parameter, and returning an Array with three elements:
he HTTP response code
A Hash of headers
The response body, which must respond to each

### Write a simple Rack application.

```
require 'rack'

app = Proc.new do |env|
  ['200', {'Content-Type' => 'text/html'}, ['A barebones rack app.']]
end

Rack::Handler::WEBrick.run app
```

### How does Rack middleware works?
Rack middleware is a way to filter a request and response coming into your application. A middleware component sits between the client and the server, processing inbound requests and outbound responses, but it's more than interface that can be used to talk to web server. It’s used to group and order modules, which are usually Ruby classes, and specify dependency between them. Rack middleware module must only: – have constructor that takes next application in stack as parameter – respond to “call” method, that takes environment hash as a parameter. Returning value from this call is an array of: status code, environment hash and response body.

### What is MVC and how it works?
- TODO:answear

### What is RailsEngine?
- TODO:answear

### What are Strong Parameters?
- TODO:answear

### What is Object-Relational Mapping?
- TODO:answear

### Describe Active Record conventions.
- TODO:answear

### Explain the Migrations mechanism.
- TODO:answear

### Describe types of associations in Active Record.
- TODO:answear

### Explain the difference between optimistic and pessimistic locking.
- TODO:answear


