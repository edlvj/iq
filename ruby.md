# RUBY QUESTIONS

### What is a class in Ruby?
In ruby its a object, abstraction data typy with it we can describe object around us. For Example Car or Animals.

### What is the difference between a class and a module?
Modules are about providing methods that you can use across multiple classes - think about them as "libraries" . 
Classes are about objects; modules are about functions.

### What is Eigenclass in Ruby?
A hidden class associated with each specific instance of another class.
```
class << foo
	# do something with the eigenclass of foo
end
```

### How to create a Sigleton in Ruby?
???


### Explain what singleton methods in Ruby?
Singleton methods in ruby are to add beviahore to one object to class

### What differents in load and require?
The load method simply reads and parses another files into your code every time a script is executed.
main difference is that require will only load the passed in file one time, and then remember that file has been loaded.
For this reason, require is the more popular option when you are using third-party libraries in your program or application

### When we need use prepend?
It actually works like include, except that instead of inserting the module between the class and its superclass in the chain, it will insert it at the bottom of the chain, even before the class itself.

### Different with Proc and Lamda.
Before I get into the differences between procs and lambdas, it is important to mention that they are both Proc objects.
Lambdas check the number of arguments, while procs do not.
Lambdas and procs treat the ‘return’ keyword differently.

### What modificate string .concat or +=?
'+' created new object every time and '.concat' works on the same object.

### What doing “frozen_string_literal”?
-  directive frozen_string_literal in file
makes all variables in file frezzed.

### What Differents in extend and include?

include - By default, it mixes in the specified module's methods as instance methods in the target module/class. E.g.
extend - adds the specified module's methods and constants to the target's metaclass

### Describe the difference between class and instance variables?

Instance Variables: Instance variables are available across methods for any particular instance or object. That means that instance variables change from object to object. Instance variables are preceded by the at sign (@) followed by the variable name.
Class Variables: Class variables are available across different objects. A class variable belongs to the class and is a characteristic of a class. They are preceded by the sign @@ and are followed by the variable name.

### What are the three levels of method access control for classes and what do they signify?

- Public methods can be called by everyone - no access control is enforced. A class's instance methods (these do not belong only to one object; instead, every instance of the class can call them) are public by default; anyone can call them. The initialize method is always private.
- Protected methods can be invoked only by objects of the defining class and its subclasses. Access is kept within the family. However, usage of protected is limited.
- Private methods cannot be called with an explicit receiver - the receiver is always self. This means that private methods can be called only in the context of the current object; you cannot invoke another object's private methods.

### What does ‘self’ mean?
self: The receiver object of the current method.
Used for static methods in ruby.

### What is Memoisation in ruby?

Memoisation is to make sure that instance variables in a method only get set once regardless of how many times the method is called.
```
@users ||= Users.all
```

### What’s Object Marshalling in ruby?

Object Marshalling is serialization.

### What is Fiber?

Fibers are light weight primitives in the Ruby standard library which can be paused, resumed and scheduled manually. They are pretty much the same as ES6 Generators if you’re familiar with JavaScript.

### When we are must use EventMachine?

EventMachine (aka EM) is a gem which is written in C++ and Ruby. It provides event-driven I/O using the Reactor pattern and can basically make your Ruby code looks like Node.js

One common reason to use EventMachine is the case when you have a lot of I/O operations and you don’t want to deal with threads manually. Manually handling threads can be difficult or often too expensive from a resource usage point of view. With EM you can handle multiple HTTP requests with a single thread by default.

### Difference between String and Symbols.

The diffence that String id mutable and Symbols not.

### Write own each_slice?
```
module Enumerable
  def each_slice(count)
    elements = self
    
    elements.pop(count) do |slice|
      yield
      break if slice.empty?
    end
    
  end
end
```

### Diffrence between .clone and .dup?
TODO

### Difference between protected, private and public in Ruby?
TODO

### What in ruby immutable and unmutable?
TODO

### What diffence between string and symbol?
TODO







