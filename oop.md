# OOP

### Basic Concepts of OOPs?

The Basic Concepts of OOP is ecapsulation, inheritance and polymorphism.

### What is a class?

Сlass is a data structure that contains data fields, like a record, as well as various methods which operate on the contents of the record.

### What is an object?

Is instance of a class.

### What is Encapsulation?

It’s mechanism for restricting direct access to some of the object's components

### What roles perform inheritance?

inheritance is when an object or class is based on another object (prototypal inheritance) or class (class-based inheritance), using the same implementation.

### Different between method overriding and method overloading?

Overloading occurs when two or more methods in one class have the same method name but different parameters. Overriding means having two methods with the same method name and parameters (i.e., method signature). One of the methods is in the parent class and the other is in the child class.

### What are the mechanisms in OOP languages that usually allow provide encapsulation of objects?

Using Private, public, protected keywords.

### Describe S.O.L.I.D?

These five principles were called the S.O.L.I.D principles (the acronym was derived by Michael Feathers).

S: Single Responsibility Principle
O: Open-Closed Principle
L: Liskov Substitution Principle
I: Interface Segregation Principle
D: Dependency Inversion Principle
S: A class should be responsible for only one thing. If a class has more than one responsibility, it becomes coupled. A change to one responsibility results to modification of the other responsibility.

O: In object-oriented programming, the open/closed principle states "software entities (classes, modules, functions, etc.) should be open for extension, but closed for modification";[1] that is, such an entity can allow its behaviour to be extended without modifying its source code.

L: The aim of this principle is to ascertain that a sub-class can assume the place of its super-class without errors. If the code finds itself checking the type of class then, it must have violated this principle.

I: This principle deals with the disadvantages of implementing big interfaces.

D: There comes a point in software development where our app will be largely composed of modules. When this happens, we have to clear things up by using dependency injection. High-level components depending on low-level components to function.

### What is Multiple inheritance?

Multiple inheritance is a feature of some object-oriented computer programming languages in which an object or class can inherit characteristics and features from more than one parent object or parent class.
It is distinct from single inheritance, where an object or class may only inherit from one particular object or class.

For example in C++
```
class C: public B, public A  // Note the order
{
public:
  C()  { cout << "C's constructor called" << endl; }
};
```

### What is Composition?

Composition is one of the fundamental concepts in object-oriented programming. It describes a class that references one or more objects of other classes in instance variables. This allows you to model a has-a association between objects.

Example:
```
driver = Driver.new
car = Car.new(driver)

```

### What the difference between abstract class and interface?

The abstract class inheritance is used when the derived class shares the core properties and behaviour of the abstract class. The kind of behaviour that actually defines the class.

On the other hand interface inheritance is used when the classes share peripheral behaviour, ones which do not necessarily define the derived class.

### What is Duck Typing?

The idea is that you don't need a type in order to invoke an existing method on an object - if a method is defined on it, you can invoke it.
The name comes from the phrase "If it looks like a duck and quacks like a duck, it's a duck".

### What is Dependency Injection?
Dependency injection is a technique whereby one object (or static method) supplies the dependencies of another object. A dependency is an object that can be used.


Here is the same code, rewritten as a class with DI:
```
class RegisterUser
  attr_reader :validator, :repo

  def initialize(validator:, repo:)
    @validator = validator
    @repo = repo
  end

  def call(params)
    if validator.validate(params)
      repo.save(params)
    else
      nil
    end
  end
end
```

The class is no longer directly coupled to its dependencies. The dependencies are passed in (injected) as arguments to initialize, and they are stored in instance variables.

Different dependencies can be passed in.
The class is independent. It can be tested in isolation, or extracted into a separate gem.
All dependencies are explicitly listed as arguments to initialize.


### Differnce between Bridge and Adapter Pattern.


