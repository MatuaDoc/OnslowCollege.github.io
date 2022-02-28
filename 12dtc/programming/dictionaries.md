---
title: Dictionaries
learning_intentions: ["Learn how to store data with a string index using dictionaries", "Access values inside dictionaries"]
success_criteria: ["You have stored data in a dictionary", "You have accessed data from within a dictionary"]
---

# Dictionaries

A standard data structure in Computer Science is the associative array which are also known as hashes or maps. In Python this is called the dictionary. 

Like lists, dictionaries can easily be changed, shrunk and grown at run time. Dictionaries can be contained in lists and vice versa.

## Lists vs Dictionaries

Lists are ordered sets of objects, whereas dictionaries are unordered sets. The main difference is that items in dictionaries are accessed via keys and not via their position.

When you have key-value-pairs, the **key** of the dictionary is associated (or mapped) to a **value**. Keys are usually strings, while values can be any Python data type.

# How to create a dictionary

Let's create a dictionary of countries and their national food. In Python you declare a dictionary using a brace (curly bracket) and separate each item using a comma.

```python
national_foods = {"Italy": "Pizza", "Japan": "Sashimi", "Spain": "Paella", "Samoa": "Panipopo"}
```

The line above has declared a dictionary called countries with 4 pieces of data.

## Storing different types of data

Python is flexible. You can use all kinds of data types for both keys and values. You are free to mix and match data to suit your needs. For example, the dictionary below contains the population of each country stored as an integer:

```python
national_population = {"Italy": 60314896, "Japan": 125837638, "Spain": 46784706, "Samoa": 200593}
```

## Storing other collections

You can treat dictionaries like a sort of 2D collection, similar to a 2D list. Dictionaries can contain lists and even other dictionaries as their values. Lists can also contain dictionaries.

```python
# Dictionary of lists
ducks = {"boys": ["Hubert", "Dewford", "Llewellyn"], "girls": ["Webbigail", "Lena", "Violet"]}

# Dictionary of dictionaries
boys = {"huey": {"long_name": "Hubert", "short_name": "Huey"}, "dewey": {"long_name": "Dewford", "short_name": "Dewey"}, "louie": {"long_name": "Llewellyn", "short_name": "Louie"}}

# List of dictionaries
girls = [{"long_name": "Webbigail", "short_name": "Webby"}]
```

## Converting two lists to a dictionary

You can use the ``zip()`` and ``dict()`` functions to convert two lists to a dictionary.

```python
countries = ["Italy", "Japan", "Spain", "Samoa"]
foods = ["Pizza", "Sashimi", "Paella", "Panipopo"]

national_foods = dict(zip(countries, foods))
```