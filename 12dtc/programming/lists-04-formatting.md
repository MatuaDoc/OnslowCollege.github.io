---
title: List formatting
---

## Learning intentions

- Formatting the printed output of a list

## Success criteria

You will know that you have completed this lesson's learning when:

- You have printed a list with custom formatting
- You have printed a list slice with custom formatting

# 4.1 Joining a list into a string

You can join all the items of a list into a single string. This will let you format the items in the list for printing.

## 4.1.1 Without ``join()``

```python
insects = ["Beetle", "Cockroach", "Fly", "Grasshopper"]
print(insects)
```

If you print the list directly like this, the result is: ``['Beetle', 'Cockroach', 'Fly', 'Grasshopper']``

However, you can format the list items using a string's ``join()`` function.

## 4.1.2 With ``join()``

```python
insects = ["Beetle", "Cockroach", "Fly", "Grasshopper"]
joined = ", ".join(insects)
print(joined)
```

This will show: ``Beetle, Cockroach, Fly, Grasshopper``

You could even use a sentence.

```python
joined = "-*quack*-".join(insects)
```

This would result in: ``Beetle-*quack*-Cockroach-*quack*-Fly-*quack*-Grasshopper``