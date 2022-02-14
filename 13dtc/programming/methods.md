---
title:  Methods
learning_intentions: ["What a method is", "How to declare an instance method"]
success_criteria: ["You have declared an instance method in a class", "You have called a method on an object"]
---

# What is a method?

In object-oriented programming, a **method** is a function that is attached to a class/object. Typically, methods operate on members stored within the class/object.

Methods exist in opposition to **free functions** which is what you have learnt so far. Free functions are not declared as part of a class.

## Examples

To explain methods, let's use an example: animals making sounds. Imagine we have a ``Duck`` class.

```python
@dataclass
class Duck:
    animal_sound = "Quack"
```

Suppose we have an instance of the ``Duck`` class and we want to make it quack. You could use a free function, ``print()``, like so:

```python
my_duck = Duck()
print(my_duck.animal_sound) # Quack
```

However, we can associate a function with the class that prints the message out for us. Here is the ``make_sound()`` method:

```python
@dataclass
class Duck:
    animal_sound = "Quack"

    def make_sound(self):
        print(self.animal_sound)

my_duck = Duck()
duck.make_sound() # Quack
```

# A special argument: ``self``

Notice the method's declaration. It accepts an argument, ``self``. Furthermore, ``self`` is used within the method definition.

The ``self`` argument is a reference to the object itself. It is how you can refer to other members or methods within the object.

All methods must contain ``self`` as the first argument in order to be called on an object.

# Methods do what functions do

Just the same as functions, methods can:
1. modify members
2. accept arguments
3. return values

## Modify variables

```python
@dataclass
class Duck:
    animal_sound = "Quack"

    # 1. Modify variables
    def set_animal_sound(self, new_sound):
        self.animal_sound = new_sound

    # 2. Accept arguments
    def make_sound(self, number_of_times=1):
        print(self.animal_sound * number_of_times)

    # 3. Return values
    def first_letter_of_animal_sound(self):
        return self.animal_sound[0]
```

# Properties are methods

Did you notice that [properties](02.members-and-properties.md) are also methods? Let's add an ``animal_sound`` property for the ``Duck`` class:

```python
@dataclass
class Duck:
    _animal_sound = "Quack"

    @property
    def animal_sound(self):
        return self._animal_sound

    @property.setter
    def animal_sound(self, new_sound):
        self._animal_sound = new_sound
```

Notice that the properties also contain the reference to ``self`` in the method declarations.

# Static methods

There is one type of method you can write that does **not** require ``self``. This is because the function is called on the class itself, not the object. This is called a **static method**.

Static methods are useful when you would like to generate some information or perform a task that is related to a class but does not work with any variables. For example, the method could generate some data in a convenient fashion, such as a list of random numbers:

```python
@dataclass
class Dog:
    name: str
    age: int

    # Normal method that uses object data
    def bark() -> str:
        return name + ", woof!"

    @staticmethod
    def generate_collar_serial() -> str:
        serial = ""
        for i in range(10):
            serial = serial + str(randint(10))
        return serial

spot = Dog(name="Spot", age=7)
spot.bark() # Spot, woof!

# Call to static method
serial = Dog.generate_collar_serial()
```

{% include task.html task_code="potato" %}