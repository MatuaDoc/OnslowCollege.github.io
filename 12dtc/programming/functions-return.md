---
title: Returning Values from a Function
learning_intentions: ["Make a function return a value"]
success_criteria: ["You have made a function return a value", "You have used that value in your code"]
---

# Returning values from a function

Instead of making all the variables you want to modify into globals, it's sometimes more useful to return a value instead. This means that the value that is returned can be stored in a variable.

To return a value, add the ``return`` keyword followed by the value to return. For example, to change the ``get_user_menu_choice()`` function to return the value rather than modify the ``choice`` variable:

```python
def get_user_menu_choice():
    print("Choose an option:")
    print("(1): Add an item")
    print("(2): Delete an item")
    print("(3): List all items")

    # Create a new value.
    new_choice = input("Type a number: ")

    # Return the value.
    return new_choice

# Calling the function returns the value
# so we can store it in a variable or print it.
choice = get_user_menu_choice()
print(choice)
```

# Specifying a return type

New to recent versions of Python, you can specify what type of data a function will return. This will make it clear to you whether or not a function provides an integer, floating-point number, string, Boolean value, etc.

To do this, add ``-> type`` to the end of the function signature (the first line). Replace ``type`` with any of the following:

| Type | Description |
| :-- | :-- |
| ``int`` | integer (whole number) |
| ``float`` | floating-point number (decimal) |
| ``str`` | string |
| ``bool`` | Boolean value (``True``/``False``) |
| ``list`` | list of any type |
| ``dict`` | dictionary of any type |

# Documenting the return type

It is also good practice to document what type of data a function returns. This makes it available to programmers who browse your code's documentation.

If your function returns a value, modify the docstring to state what it **returns** and in what type.

| Before | After |
| :-- | :-- |
| Sets the user's menu choice | **Returns** the user's menu choice as an int |

This information becomes available when a user hovers over a function in Visual Studio Code.

![Returning function's documentation](img/function-tool-tip-return.png)