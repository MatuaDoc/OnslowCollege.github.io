---
title: Cheat Sheet
---

# Object Oriented Programming

## Dataclass

```python
from dataclasses import dataclass

@dataclass
class MyDataclass:
    """
    Docstring that explains what MyClass is about.
    """

    # Members
    _my_protected_string: str
    _my_protected_number: int
    _my_protected_bool: bool
```

## Properties

### Getter for a member

```python
@property
def my_string(self) -> str:
    return self._my_protected_string
```

See also [Accessing object data](#accessing-object-data)

### Getter that does not represent a member

```python
@property
def half_price(self) -> float:
    return self._my_protected_number / 2
```

See also [Accessing object data](#accessing-object-data)

### Setter (no validation)

```python
@my_string.setter
def my_string(self, new_string: str):
    self._my_protected_string = new_string
```

See also [Updating object data](#updating-object-data)

### Setter (with validation)

```python
@my_string.setter
def my_string(self, new_string: str):
    """
    Docstring that explains the validation.
    i.e. Sets the string if it has at least 1 character.
    """

    # Checks that new_string has at least 1 character.
    # Otherwise, raises a ValueError
    if len(new_string) > 0:
        self._my_protected_string = new_string
    else:
        raise ValueError("String must contain at least 1 character")
```

See also [Updating object data](#updating-object-data)

## Methods

### Instance method

```python
@dataclass
class MyClass:
    _my_protected_string: str

    def my_method(self, arg1: int, arg2: SomeClass) -> bool:
        """
        Docstring that explains what the function does, what each argument
        is for, and what the returned value represents.

        Arguments:
        - arg1 (int): a very fancy number
        - arg2 (SomeClass): an object of SomeClass

        Returns:
        - True if arg1 is above 0 or some_property is present in arg2
        - Otherwise, False
        """
        if arg1 > 0:
            return True
        elif arg2.some_property:
            return True
        else:
            return False
```

See also [calling an instance method](#calling-an-instance-method)

## Creating an object

### Storing one object in a variable

```python
my_object = MyClass("Hello", 23, False)
```

### Storing multiple objects in a list

```python
my_objects = [
    MyClass("Hello", 23, False),
    MyClass("Goodbye", 27, True),
    MyClass("42", 42, True)
]
```

### Generating multiple objects using a loop

```python
my_objects = []
for i in range(0, 10):
    my_objects.append(MyClass("Hello", i, False))
```

### Generating multiple objects using a list comprehension

```python
my_objects = [MyClass("Hello", i, False) for i in range(0, 10)]
```

## Working with object data

### Accessing data from a single object

```python
print(my_object.string)
```

### Accessing data from multiple objects using a loop

```python
strings = []
for each_object in my_objects:
    strings.append(each_object.string)
print(strings)
```

### Accessing data from multiple objects using a list

```python
strings = [each_object.string for each_object in my_objects]
print(strings)
```