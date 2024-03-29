# Deployment and Server Managment
# Deployment

### What is Upstart in Linux.
Upstart is an event-based replacement for the traditional init daemon – the method by which several Unix-like computer operating systems perform tasks when the computer is started.

### What is Ansible and how it works.
Ansible is an open-source software provisioning, configuration management, and application deployment tool.
Ansible is agentless - temporarily connecting remotely via SSH or remote PowerShell to do its tasks

### What is Capistrano and how it works.
Capistrano is a framework for building automated deployment scripts.
A remote server automation and deployment tool written in Ruby

### What is Amazon S3?
Amazon Simple Storage Service is storage for the Internet. It is designed to make web-scale computing easier for developers.

Amazon S3 has a simple web services interface that you can use to store and retrieve any amount of data, at any time, from anywhere on the web. It gives any developer access to the same highly scalable, reliable, fast, inexpensive data storage infrastructure that Amazon uses to run its own global network of web sites. The service aims to maximize benefits of scale and to pass those benefits on to developers.

### What Type of Deployment Code You Know in EB?
Deployment policy – Choose from the following deployment options:

All at once – Deploy the new version to all instances simultaneously. All instances in your environment are out of service for a short time while the deployment occurs.

Rolling – Deploy the new version in batches. Each batch is taken out of service during the deployment phase, reducing your environment's capacity by the number of instances in a batch.

Rolling with additional batch – Deploy the new version in batches, but first launch a new batch of instances to ensure full capacity during the deployment process.

Immutable – Deploy the new version to a fresh group of instances by performing an immutable update.

### What are the types of design patterns you know?
There are three types of design patterns. They are:

Creational Patterns: These patterns provide freedom of choice between creating objects by hiding the logic. The objects constructed are decoupled from the implemented system. Some of the examples of creational patterns are - Factory design pattern, Builder design, Prototype design, Singleton design, Abstract Factory design.
Structural Patterns: These patterns help in defining how the structures of classes and objects should be like for defining the composition between classes, interfaces and objects. Some of the examples of structural patterns are - Adaptor design, Facade design, Decorator design, proxy design etc.
Behavioural Patterns: These patterns help to define how the objects should communicate and interact with one another. Some of the examples of behavioural patterns are - Command pattern, Iterator pattern, Observer pattern, Strategy pattern, etc.
