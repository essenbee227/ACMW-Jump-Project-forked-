---
title: Python OOP (Object-Oriented Programming)
sidebar_label: Python OOP 
description: A discussion on Pythons Object Oriented Programming and the Key concepts 
---

# Python Object-Oriented Programming (OOP)

![OOP](/img/images.png)

Object-Oriented Programming (OOP) is a programming paradigm that organizes code into reusable structures called objects. Python, being an object-oriented language, allows developers to write modular and scalable code using OOP principles.

 By understanding the core OOP principles (classes, objects, inheritance, encapsulation, polymorphism, and abstraction), programmers can use the full potential of Python OOP capabilities to design elegant and efficient solutions to complex problems.

### Key OOP Concepts in Python

#### 1. Classes and Objects

A class is a blueprint for creating objects, while an object is an instance of a class.
```
class Car:
    def __init__(self, brand, model, year):
        self.brand = brand
        self.model = model
        self.year = year

    def display_info(self):
        return f"{self.year} {self.brand} {self.model}"
        
my_car = Car("Toyota", "Corolla", 2022)
print(my_car.display_info())
```

* **class Car**: Defines a class named car

* `__init__ method`: intializes the brand, model, and year when a new opbject is created.

* **Output**

`Toyota
Corolla`

#### 2. Encapsulation

Encapsulation restricts direct access to certain variables and methods, ensuring better security and code integrity.

**Types of Encapsulation**
* Public Members: Accessible from anywhere.
* Protected Members: Accessible within the class and its subclasses.
* Private Members: Accessible only within the class.
```
class BankAccount:
    def __init__(self, balance):
        self.__balance = balance  # Private attribute

    def deposit(self, amount):
        self.__balance += amount
        return f"Deposited {amount}. New balance: {self.__balance}"

    def get_balance(self):
        return self.__balance

account = BankAccount(1000)
print(account.deposit(500))
print(account.get_balance())
```

#### 3. Inheritance

Inheritance allows one class (child) to inherit properties and methods from another class (parent).

**Types of Inheritance**
* Single Inheritance: A child class inherits from a single parent class.
* Multiple Inheritance: A child class inherits from more than one parent class.
* Multilevel Inheritance: A child class inherits from a parent class, which in turn inherits from another class.
* Hierarchical Inheritance: Multiple child classes inherit from a single parent class.
* Hybrid Inheritance: A combination of two or more types of inheritance.

```
class Vehicle:
    def __init__(self, brand):
        self.brand = brand

    def honk(self):
        return "Honk! Honk!"

class Car(Vehicle):
    def __init__(self, brand, model):
        super().__init__(brand)
        self.model = model

my_car = Car("Honda", "Civic")
print(my_car.honk())  # Inherited method
```

#### 4. Polymorphism

Polymorphism allows different classes to have methods with the same name but different implementations.

**Types of Polymorphism**

* Compile-Time Polymorphism: The program's compilation determines this kind of polymorphism. It allows operators or methods of the same name to behave differently depending on their use or input parameters. It is often called operator overloading or method overloading.

* Run-Time Polymorphism: This kind of polymorphism is identified while the program is running. Method overriding is the process by which a subclass offers a particular implementation for a method that is already declared in its parent class.
```
class Dog:
    def sound(self):
        return "Bark"

class Cat:
    def sound(self):
        return "Meow"
        
for animal in [Dog(), Cat()]:
    print(animal.sound())
```

#### 5. Abstraction

Abstraction hides complex implementation details and exposes only the necessary parts of an object.

**Types of Abstraction**

* Partial Abstraction: Abstract class contains both abstract and concrete methods.

* Full Abstraction: Abstract class contains only abstract methods (like interfaces).

```
from abc import ABC, abstractmethod

class Animal(ABC):
    @abstractmethod
    def sound(self):
        pass

class Dog(Animal):
    def sound(self):
        return "Bark"

my_dog = Dog()
print(my_dog.sound())
```

### Benefits of OOP in Python

* Code Reusability: Classes and objects promote modularity.

* Scalability: Large applications can be structured efficiently.

* Security: Encapsulation restricts direct data modification.

* Readability: OOP improves code organization and maintainability.

### Conclusion

OOP is a fundamental concept in Python that enables developers to create clean, efficient, and scalable applications. 
