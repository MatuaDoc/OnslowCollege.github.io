---
title: Functions
learning_intentions: ["Reduce repeated code with functions", "Define a function", "Make the function return a value"]
success_criteria: ["You have defined a function", "You have made the function return a value"]
---

# Functions

There are times when your code becomes repetitive. For example, if you ask the user multiple times throughout the program for text, you will find yourself:

1. checking that the user has typed in something
2. checking that what the user entered is valid
3. doing some calculations or running some logic based on what the user entered
4. doing it all over again later in the program!

## How to write a function

```python
def function_no_args():
    # Code goes here
```

1. Start the line with ``def``. This means function **def**inition
2. Give the function a name. Make it descriptive, all lowercase, and in ``snake_case`` (underscores, no spaces)
3. Add a left parenthesis, right parenthesis, and a colon ``():``
4. Indented to the right, you can write as much code as you want

# Modifying variables declared outside the function

To be able to change variables that are defined outside the function, you need to declare the variable as **global** so that the function is able to access and modify it.

To do that, add the following line to your function's code:

```python
global variable_name
```

You **DON'T** need to declare variables as global if:
- they are declared outside the function **but** you don't modify them
- they are declared inside the function

For example, a function that prints a menu and asks the user to choose an item:

```python
# Defined outside the function
choice = ""

def get_user_menu_choice():
    global choice
    print("Choose an option:")
    print("(1): Add an item")
    print("(2): Delete an item")
    print("(3): List all items")
    while choice == "":
        choice = input("Type a number: ")
```

## Calling a function

You can **call** a function that you have defined in your code at any time. To do this, you specify the name of the function including the parentheses.

For example, to call the function defined above:

```python
choice = ""

# Call the function
get_user_menu_choice()

if choice == "1":
    # do this
elif choice == "2":
    # do that
else:
    # do the other
```

# Returning values from a function

Instead of making all the variables you want to modify into globals, it's sometimes more useful to return a value instead. This means that the value that is returned can be stored in a variable.

To return a value, add the ``return`` keyword followed by the value to return. For example, to change the ``get_user_menu_choice()`` function to return the value rather than modify the ``choice`` variable:

```python
def get_user_menu_choice():
    print("Choose an option:")
    print("(1): Add an item")
    print("(2): Delete an item")
    print("(3): List all items")
    new_choice = input("Type a number: ")
    return new_choice

# Since get_user_menu_choice() now returns a value, the returned
# value can be assigned to the choice variable directly.
choice = get_user_menu_choice()
```