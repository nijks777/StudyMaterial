Object-Oriented Programming (OOP) Interview Questions - Java/Python
EASY (5 Questions)

What are the four main principles of Object-Oriented Programming? Explain each briefly.
What is the difference between a class and an object? Provide examples in both Java and Python.
What is the difference between method overloading and method overriding?
Explain the concept of encapsulation. Why is it important?
What is a constructor? What is the difference between a default constructor and a parameterized constructor?


MEDIUM (15 Questions)

Explain the difference between abstraction and encapsulation with real-world examples.
What is polymorphism? Explain compile-time (static) polymorphism and runtime (dynamic) polymorphism.
Scenario: You're designing a payment system that needs to support multiple payment methods (Credit Card, PayPal, Cryptocurrency). How would you use polymorphism to implement this?
What is the difference between an abstract class and an interface? When would you use each?
Explain the concept of inheritance. What are the different types of inheritance, and which ones are supported in Java and Python?
What is the difference between composition and inheritance? When should you favor composition over inheritance?
Scenario: You have a Vehicle class and need to create Car, Bike, and Truck classes. Should you use inheritance or composition? Justify your answer.
What is the diamond problem in multiple inheritance? How does Python handle it, and why doesn't Java allow multiple inheritance of classes?
Explain the concept of method resolution order (MRO) in Python. How does it work?
What are access modifiers? Explain public, private, protected, and default (Java) / name mangling in Python.
What is the difference between static methods, class methods, and instance methods? Provide examples in both Java and Python.
Scenario: You're building a logging system that should have only one instance throughout the application. Which design pattern would you use and how would you implement it?
What are magic/dunder methods in Python (like __init__, __str__, __repr__)? What are their Java equivalents?
Explain the concept of coupling and cohesion. How do they relate to good OOP design?
What is the difference between deep copy and shallow copy when dealing with objects?


HARD (10 Questions)

Scenario: You're designing a notification system that can send notifications via Email, SMS, and Push. New notification types may be added in the future. Users should be able to subscribe to multiple notification types. Design this system using OOP principles and explain your design choices.
Explain the SOLID principles in detail. Provide a practical example of violating and then fixing each principle.
What is the Liskov Substitution Principle? Provide an example where this principle is violated and how to fix it.
Scenario: You have a Rectangle class with setWidth() and setHeight() methods. You create a Square class that inherits from Rectangle. Is this a good design? Why or why not? How does this relate to LSP?
Explain the difference between aggregation and composition. Provide code examples demonstrating the lifecycle differences.
What are design patterns? Explain the Factory Pattern, Strategy Pattern, and Observer Pattern with real-world use cases.
Scenario: You're building an e-commerce system with products, orders, payments, and shipping. Multiple products can be in an order, an order has one payment, and one shipping method. Design the class structure considering relationships (has-a, is-a), and explain your reasoning.
What is covariance and contravariance in the context of generics (Java) or type hints (Python)? How do they affect method overriding?
Scenario: You have a legacy codebase where a Bird class has a fly() method. Now you need to add Penguin and Ostrich which can't fly. How would you refactor this design to follow OOP principles properly?
Explain the differences between early binding and late binding. How does this relate to polymorphism? What are the performance implications? How do abstract base classes (ABC) in Python and interfaces/abstract classes in Java enforce contracts?