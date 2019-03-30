# RUBY QUESTIONS

### What is a class in Ruby?
In ruby its a object, abstraction data typy with it we can describe object around us. For Example Car or Animals.

### What is the difference between a class and a module?
Modules are about providing methods that you can use across multiple classes - think about them as "libraries" . Classes are about objects; modules are about functions.

### What is Eigenclass in Ruby?
- TODO:answear

### Explain what singleton methods in Ruby?
singleton methods in ruby are to add beviahore to one object to class

### What Differents in load and require?
TODO:answear

### Different with Proc and Lamda.
Before I get into the differences between procs and lambdas, it is important to mention that they are both Proc objects.
Lambdas check the number of arguments, while procs do not.
Lambdas and procs treat the ‘return’ keyword differently.

### What modificate string .concat or +=?
'+' created new object every time and '.concat' works on the same object.

### When we need use prepend?
- TODO:answear

### Then we can use frezze or dup.
- TODO:answear

### What doing “frozen_string_literal”?
 - TODO:answear

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

### What is Memoisation in ruby?
- TODO:answear

### What is Fiber?
- TODO:answear





