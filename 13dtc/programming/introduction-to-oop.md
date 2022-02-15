---
title:  Introduction to object-oriented programming
learning_intentions: ["What benefits object-oriented programming can provide", "How to define a class", "How to instantiate a class to create an object"]
success_criteria: ["You have completed the Intro to OOP task"]
---
 
# What is object-oriented programming?

In year 13, you will be expected to use object-oriented programming techniques as part of the computer program standard.

> Object-oriented programming (OOP) is a way of writing computer programs using "objects" to stand for **data and methods**. Computer programs that are not object-oriented are a list of instructions for the computer, telling it to do certain things in a certain way, which is called procedural programming. However, in object-oriented programming, computer programs use objects that talk to one another to change the data in those objects […]  Because of the way object-oriented programming is designed, it helps the developer by allowing for code to be easily reused by other parts of the program or even by other people.[^1]

As stated by the definition above, object-oriented programming is another way to write programs. So far, you've written programs as a series of steps one after the other — variables get declared, some code might update the values, and so on until the program closes.

But ask yourself these questions. How can you determine:

- what variables are related to each other?
- which functions can use the variables and which cannot?
- when the variable is no longer required?

Without objects, any variables that we declare are effectively available to any code in the same scope, including functions. This means that a variable's value may change at some point and, short of printing a statement every time any variable's value changes, we can't be entirely sure what variables have changed or what piece of code caused the change.

# Classes and objects

## Classes

In object-oriented programming, **classes** allow us to collect related data and functions into an object. In terms of the data, we can also decide what information we want to expose to the rest of the program or even to the programmer.

For example, we can create a class that keeps the information for a student in one place:

```python
from dataclasses import dataclass

@dataclass
class Student:
    """Personal information for a student"""
    name: str
    age: int
```

Just like this, we ensure that the name and age are in one place.

With some additional work, we can also prevent code outside of the class from modifying the data. This is done in conjuction with methods.

## Objects

This is all great but how do we actually *use* the class? To actually use the ``Student`` class, we *instantiate* it: this means that we create an **object** based on the class.

Remember: if the class is a blueprint for something, the object is the actual thing!

```python
from dataclasses import dataclass

# Create a class called Student
@dataclass
class Student:
    """Personal information for a student"""
    name: str
    age: int

# Create a Student object called student1
student1 = Student(name="Alan", age=17)

# Print the student1 object's age and name
print(student1.age) # 17
print(student1.name) # Alan

# Change the student1 object's value
student1.name = "Zack"

# Print the student1 object's age and name after change
print(student1.age) # 17
print(student1.name) # Zack
```

{% include task.html task_code="UirLo6m3" %}

[^1]: Adapted from [Object-oriented programming](https://simple.wikipedia.org/wiki/Object-oriented_programming), Simple English Wikipedia (retrieved 15/11/2021, emphasis added).
