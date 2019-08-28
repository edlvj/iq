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
MVC is a pattern for the architecture of a software application. It separates an application into the following components:

- Models for handling data and business logic
- Controllers for handling the user interface and application
- Views for handling graphical user interface objects and presentation

### What is Rails Engine?
Engines can be considered miniature applications that provide functionality to their host applications. A Rails application is actually just a "supercharged" engine, with the Rails::Application class inheriting a lot of its behavior from Rails::Engine.

Therefore, engines and applications can be thought of as almost the same thing, just with subtle differences, as you'll see throughout this guide. Engines and applications also share a common structure.

Engines can also be isolated from their host applications. This means that an application is able to have a path provided by a routing helper such as articles_path and use an engine that also provides a path also called articles_path, and the two would not clash. Along with this, controllers, models and table names are also namespaced. You'll see how to do this later in this guide.

### What are Strong Parameters?
Action Controller parameters are forbidden to be used in Active Model mass assignments until they have been permitted. This means that you'll have to make a conscious decision about which attributes to permit for mass update. This is a better security practice to help prevent accidentally allowing users to update sensitive model attributes.

### What is Object-Relational Mapping and Active Record?
Object Relational Mapping, commonly referred to as its abbreviation ORM, is a technique that connects the rich objects of an application to tables in a relational database management system. Using ORM, the properties and relationships of the objects in an application can be easily stored and retrieved from a database without writing SQL statements directly and with less overall database access code.

Active Record gives us several mechanisms, the most important being the ability to:

- Represent models and their data.
- Represent associations between these models.
- Represent inheritance hierarchies through related models.
- Validate models before they get persisted to the database.
- Perform database operations in an object-oriented fashion.

### Describe Active Record conventions.
Rails will pluralize your class names to find the respective database table. So, for a class Book, you should have a database table called books. The Rails pluralization mechanisms are very powerful, being capable of pluralizing (and singularizing) both regular and irregular words. When using class names composed of two or more words, the model class name should follow the Ruby conventions, using the CamelCase form, while the table name must contain the words separated by underscores. Examples:

Database Table - Plural with underscores separating words (e.g., book_clubs).
Model Class - Singular with the first letter of each word capitalized (e.g., BookClub).

### Explain the Migrations mechanism.
With the help of rails migration, we can make changes in the database schema which makes it possible to use the version control system for synchronization of those things with the actual code. 

Rails migration can perform the following things:
It helps in creating the table for the database.
1. Dropping the table is possible with the help of this.
2. Renaming of the table is possible.
3. We can even add columns.
4. Renaming of the columns can be done.
5. Columns can be changed too.
6. We can remove the columns and various other things can be done.

### Describe types of associations in Active Record.
- The belongs_to Association
- The has_one Association
- The has_many Association
- The has_many :through Association
- The has_one :through Association
- The has_and_belongs_to_many Association

### Explain the difference between optimistic and pessimistic locking.
Optimistic Locking 
assumes that a database transaction conflict is very rare to happen. It uses a version number of the record to track the changes. It raise an error when other user tries to update the record while it is lock.

Just add a lock_version column to the table you want to place the lock and Rails will automatically check this column before updating the record.

Pessimistic locking
 assumes that database transaction conflict is very likely to happen. It locks the record until the transaction is done. If the record is currently lock and the other user make a transaction, that second transaction will wait until the lock in first transaction is release.

```
user = User.lock.find(1) #lock the record
user.name = 'ryan'
user.save! #release the lock
```
or you can also use with_lock method to select and lock the record.
```
user = User.find(1)
user.with_lock do #lock the record
  # you can run other code here.
  user.name = 'ryan'
  user.save!
end
```

### Explain various forms of caching available in Rails.
https://edgeguides.rubyonrails.org/caching_with_rails.html

### What is do Spring or Zeus in Rails?
Spring and Zeus is a Rails application preloaders. It speeds up development by keeping your application running in the background so you don't need to boot it every time you run a test, rake task or migration.
Also it have features for reload code after request.

### Explain big O notation problem in Rails.
Big-O notation is just a fancy way of describing how your code's performance depends on the amount of data it's processing.

Performance means one of two things: speed, or ram usage. In computer science class you'd refer to these as "time complexity" and "space complexity." Big-O notation is used for both, but we're going to focus on speed here, since that seems to be the more common usage.

How to Avoid this in Ruby
- Finding a specific item in a Hash is faster than in an Array
- Avoid nested loops
- Watch out for accidental DB queries when generating lists in your views

### What is Railtie and that it do in ROR. 

Rails::Railtie is the core of the Rails framework and provides several hooks to extend Rails and/or modify the initialization process.

Every major component of Rails (Action Mailer, Action Controller, Active Record, etc.) implements a railtie.
- handles the bootstrapping process for a Rails application;
- manages the rails command line interface;
- and provides the Rails generators core.

### What do helpers in Rails.
Some helper classes are present in the helper sub directory which is used for assisting the view, model and the controller classes present in it.

### Describe what is background job processing and Active job. 

Active Job is a framework for declaring jobs and making them run on a variety of queuing backends. These jobs can be everything from regularly scheduled clean-ups, to billing charges, to mailings. Anything that can be chopped up into small units of work and run in parallel, really.


### For that you should use .transaction mehtod for ActiveRecord Models.

Transactions are protective blocks where SQL statements are only permanent if they can all succeed as one atomic action. The classic example is a transfer between two accounts where you can only have a deposit if the withdrawal succeeded and vice versa. Transactions enforce the integrity of the database and guard the data against program errors or database break-downs. So basically you should use transaction blocks whenever you have a number of statements that must be executed together or not at all.

Exceptions will force a ROLLBACK that returns the database to the state before the transaction began.



