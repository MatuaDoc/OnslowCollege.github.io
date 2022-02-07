---
title:  Introduction to object-oriented programming
---

## Learning intentions

You will learn:

- what benefits object-oriented programming can provide
- how to:
    - defined a class, and
    - instantiate an object from a class

### Success criteria

You will know that you have completed the learning when:

- you can correctly complete the [OOP quiz task](#task)
- 
# What is object-oriented programming?

In year 13, you will be expected to use object-oriented programming techniques as part of the computer program standard.

> Object-oriented programming (OOP) is a way of writing computer programs using "objects" to stand for **data and methods**. Computer programs that are not object-oriented are a list of instructions for the computer, telling it to do certain things in a certain way, which is called procedural programming. However, in object-oriented programming, computer programs use objects that talk to one another to change the data in those objects […]  Because of the way object-oriented programming is designed, it helps the developer by allowing for code to be easily reused by other parts of the program or even by other people.[^1]

As stated by the definition above, object-oriented programming is another way to write programs. So far, you've written programs as a series of steps one after the other — variables get declared, some code might update the values, and so on until the program closes.

But ask yourself these questions. How can you determine:

- what variables are related to each other?
- which functions can use the variables and which cannot?
- when the variable is no longer required?

Without objects, any variables that we declare are effectively available to any code in the same scope, including functions. This means that a variable's value may change at some point and, short of printing a statement every time any variable's value changes, we can't be entirely sure what variables have changed or what piece of code caused the change.

For instance, consider some variables for a program that keeps track of a student's details.

```python
student_name = ""
student_age = -1

def set_student_name():
    """Asks for a name, verifies that it is non-zero in length"""
    name = ""
    while len(name) == 0:
        name = input("Enter a name: ")
    student_name = name

def set_student_age():
    """Asks for an age, verifies that it is a valid integer"""
    age = -1
    while not age in range(11, 22):
        try:
            age = int(input("Enter an age: "))
        except:
            print("Please type a valid integer")
    student_age = age

def set_student_details():
    """Quickly sets student details"""
    student_name = input("Enter a name: ")
    student_age = input("Enter an age: ")
    # No validation!
```

Notice that we have two functions that validate the user's inputted name and age. However, there is also another function that performs no validation whatsoever. Of course, we could just fix the code to perform proper validation. Even better, it could just call the previously-defined functions that do that for us.

However, that's still no guarantee that *other* code within the program won't have the issue as the ``set_student_details()`` function. It only takes a moment of absent-mindedness or perhaps working with another programmer unfamiliar with your validation techniques to cause bugs.

# Classes and objects

## Classes

In object-oriented programming, **classes** allow us to collect related data and functions into an object. In terms of the data, we can also decide what information we want to expose to the rest of the program or even to the programmer.

For example, we can create a class that keeps the information for a student in one place:

```python
from dataclasses import dataclass

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
# Create an instance of the Student class
alan_kay = Student(name="Alan", age=17)

# Modify the alan_kay object
alan_kay.name = "Alan"

# Print the alan_kay object's age
print(alan_kay.age) # 17
```

# Task

Now it's your turn to create a class and instantiate it!

1. [Accept this Github Classroom assignment](https://classroom.github.com/a/UirLo6m3)
2. Open the repository in Visual Studio Code ([instructions here](../../Classroom/README.md))
3. Edit the code to pass the tests
4. Commit and push your code to Github for autograding

[^1]: Adapted from [Object-oriented programming](https://simple.wikipedia.org/wiki/Object-oriented_programming), Simple English Wikipedia (retrieved 15/11/2021, emphasis added).
