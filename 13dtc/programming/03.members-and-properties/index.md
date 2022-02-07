---
title:  Members and Properties
---

## Learning intentions

You will learn:

- what a class member is
  - how to declare one
- what a class property is
  - when you should use one
  - how to declare one

### Success criteria

You will know that you have completed the learning when:

- you can answer the quiz at the bottom of the page
- you have completed the [members and properties task](#task)

# What is a member?

In object-oriented programming, a **member** is a value stored in a class or object. Members include variables, constants, and [properties](##what-is-a-property).

In Python, these can be defined easily using a ``@dataclass``.

For example, the following ``Document`` class has a few members defining who wrote the document, when it was created, when it was last updated, and the text content of the document.

```python
from dataclasses import dataclass
from datetime import Date

@dataclass
class Document:
    # The following are members
    creator_name: str
    created_date: Date
    modified_date: Date
    text_content: str
```

When instantiating a ``Document`` object, the members can be accessed using [dot notation](https://www.askpython.com/python/built-in-methods/dot-notation) — the object, a dot, then the name of the member.

```python
my_document = Document("RJA", Date(), Date(), "Hello, world!")
my_document.text_content = "Bonjour, tout le monde !"
print(my_document.text_content)
```

# Properties

After creating a class, we can restrict what actions can be performed on its members — for example, we could disallow changing a member's value, ensure that only certain values can be entered, or even make it so that getting a value returns it in a specific format.

A strong benefit of this is that we fully understand what happens when a class' data is changed, how, and even why. In the example below, we modify the ``Document`` class to validate the following:

1. When changing ``creator_name``, the new string must contain at least one character
2. When updating ``modified_date``, the new date be after the existing ``modified_date`` value

```python
from dataclasses import dataclass, field
from datetime import Date

@dataclass
class Date:
    # Properties
    _creator_name: str
    created_date: Date    # Note: this is not protected, nor a property
    _modified_date: Date

    @property
    def creator_name(self) -> str:
        return self._creator_name

    @name.setter
    def creator_name(self, new_name: str):
        # Validates that the name is non-empty
        # else raises an error
        if len(new_name) > 0:
            self._creator_name = new_name
        else:
            raise ValueError("Name must contain at least one character")

    @property
    def _modified_date(self) -> int:
        return self._modified_date

    @age.setter
    def date(self, new_date: Date):
        # Validates that the age is within the correct range
        # else raises an error
        if new_date > self._modified_date:
            self._modified_date = new_date
        else:
            raise ValueError("Modified date must not precede last modification date")
```

## What's in a property?

As you can see, we create methods that do the following:

1. Protect the ``_creator_name`` and ``_modified_date`` variables from being accessed directly
2. Allow accessing the ``_creator_name`` and ``_modified_date`` safely through ``creator_name()`` and ``modified_date()`` methods
3. Allow changing the ``_creator_name`` and ``_modified_date`` **with validation** through the setter methods

But how does it actually do it?

### Step 1: Protect the variables

To start with, we modify the names of the variables to include an underscore at the front. You will notice that ``creator_name`` and ``modified_date`` have become ``_creator_name`` and ``_modified_date``.

The underscore at the front is a signal to other Python developers that the variable should not be accessed directly; rather, fetching the value and changing it should be done through the use of a property.

### Step 2: Getters and setters

#### Getters

In order to validate the data when it is changed, we first need to define a special function that returns the value of the variable. This is called a **getter**: it *gets* the variable!

```python
@property
def creator_name(self):
    return self._creator_name
```

When dealing with objects, you don't need to call the getter like a function; it behaves like a variable or constant.

```python
document = Document("Alan Partridge", Date(), Date(), "A-ha!")
print(document.creator_name) # Alan Partridge
```

It's also possible to have getters perform custom behaviours. Say we store names with normal casing but want to easily retrieve the name in all upper case letters:

```python
@property
def creator_initials(self):
    initials = []
    for word in self._creator_name.split(" "):
        initials.append(word[0])
    return ''.join(initials)
```

```python
document = Document("Alan Partridge", Date(), Date(), "A-ha!")
print(document.creator_initials) # AP
```

#### Setters

The true magic happens in **setters**. Using setters, you can validate or run custom code when a variable's value is changed.

For instance, the following examples:

1. Validate that the name contains at least one character
2. Transforms all spaces to underscores
3. All of the above

```python
@name.setter
def name(self, new_name: str):
    if len(new_name) > 0:
        self._name = new_name
    else:
        raise ValueError("Name must contain at least one character")
```

```python
@name.setter
def name(self, new_name: str):
    self._name = new_name.replace(" ", "_")
```

```python
@name.setter
def name(self, new_name: str):
    if len(new_name) > 0:
        self._name = new_name.replace(" ", "_")
    else:
        raise ValueError("Name must contain at least one character")
```

# Task

Now it's your turn to create properties in a class!

1. [Accept this Github Classroom assignment](#task)
2. Open the repository in Visual Studio Code ([instructions here](../../Classroom/README.md))
3. Edit the code to pass the tests
4. Commit and push your code to Github for autograding