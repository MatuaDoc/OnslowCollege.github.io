---
title: (Re)Intro to Python
---

**Learning Intentions**

- If you learnt Python in 11DIT, to revise the basic Python statements
  - Assigning and using variables
  - Printing text and getting input
  - Converting numbers to strings
  - Repeating code with loops
  - Checking for conditions with if statements
- If you have not learnt Python before, to get to know the basics

**Success Criteria**
 
You will know that you have completed this lesson's learning when:
-   You have created a room area calculator

--------

## Welcome (back) to Python! 🐍

If you took 11DIT at Onslow College last year, then welcome back! It's time to get our minds back into programming. Hopefully you haven't forgotten all your Python — if you have, don't worry, it's just like riding a bike! (and if you haven't been on a bike before, don't worry, it'll all come back just the same!)

--------

# Task 2.1 Room Area Calculator

> **Filename**: area.py

## 2.1.1 Requirements

In this task, you will be asked to make a program that calculates the area of a room.

- Ask the user for the length and width of the room in metres
- Convert the answers to a floating point number
- Print out the area of the room in square metres (``m²``)

## 2.1.2 First steps

1. [Accept this Github Classroom assignment](https://classroom.github.com/a/UirLo6m3)
2. Open the repository in Visual Studio Code ([instructions here](../../Classroom/README.md))
3. Edit the code to pass the tests
4. Commit and push your code to Github for autograding

## 2.1.4 Statements to use

- ``print()``
- ``input()``
- ``float()``
- ``while``
- ``if``
- ``*``

## 2.1.5 Example output

```
Enter the room width in metres: 2
Enter the room length in metres: 4.5

Your room is 9 m²
```

# Task 2.2 Convert to US units

> **Filename**: area.py

## 2.2.1 Requirements

In this task, you will be asked to improve the room area calculator with the following features:

- Ask the user if they wish to see the area in metres or feet
- Calculate the room area in both metres and feet

## 2.2.2 Statements to use

- ``*``
- ``/``
- ``if``

## 2.2.3 Hint

1 foot is 0.3048 metres. 1 metre is 3.28084 feet.

## 2.2.4 Example output

```
Enter the room width in metres: 2
Enter the room length in metres: 4.5

Type m for metres or f for feet: f

Your room is 29.52756 ft²
```

# Task 2.3 Calculate the room volume

> **Filename**: area.py

## 2.3.1 Requirements

In this task, you will be asked to improve the room area calculator with the following features:

- Ask the user if they wish to calculate the *volume* of the room
- If so, ask for the height of the room
- Print out the volume of the room in cubic metres/feet (``m³``/``ft³``)

## 2.3.2 Statements to use

- ``if``
- ``else``
- ``*``

## 2.3.3 Example output

```
Enter the room width in metres: 2
Enter the room length in metres: 4.5
Do you want to calculate the volume? y
Enter the room height in metres: 1.5

Type m for metres or f for feet: m

Your room is 13.5 m³
```

# Task 2.4 Extension: Made for US users

> **Filename**: area.py

## 2.4.1 Requirements

In this task, you will be asked to improve the room area calculator with the following features:

- Allow the user to enter the room width, length, and height in feet
- The program must still be able to calculate the area/volume in metres
- Always show the calculation in both metres **and** feet

## 2.4.2 Example output

```
Type m to enter in metres or f in feet: f
Enter the room width in feet: 7
Enter the room length in feet: 15
Do you want to calculate the volume? n

Type m for metres or f for feet: m

Your room is 105 ft² / 9.7548192 m²
```

# Task 2.5 Extension: Furniture

> **Filename**: area.py

## 2.5.1 Requirements

In this task, you will be asked to improve the room area calculator with the following features:

- Ask if the user wants to calculate the remaining volume of the room *with furniture added*
- If so, ask the user to select which furniture is in the room
  - There is a list of furniture items, each with a defined volume. Please see section 2.4.3
- Calculate the *remaining* volume of the room by subtracting the combined volume of the furniture from the total volume of the room
- If the combined furniture volume is greater than the volume of the room itself, tell the user that they need to choose an item of furniture to remove

## 2.5.2 Statements to use

- ``if``
- ``else``
- ``*``
- Constants
- Lists

## 2.5.3 Volumes

- TV
  - Width: 1.25 m
  - Height: 0.8 m
  - Depth: 0.2 m
- Sofa
  - Width: 2 m
  - Height: 1 m
  - Depth: 0.85 m
- Table
  - Width: 2 m
  - Height: 1.5 m
  - Length: 4 m
- Cabinet
  - Width: 1.5 m
  - Height: 4 m
  - Depth: 1.25 m
- Bookcase
  - Width: 1 m
  - Height: 2.5 m
  - Depth: 0.4 m

## 2.4.4 Example output

```
Enter the room width in metres: 2
Enter the room length in metres: 4.5
Do you want to calculate the volume? y
Enter the room height in metres: 1.5

Do you want to add furniture? y

Choose from the list below:
0: TV
1: Sofa
2: Table
3: Cabinet
4: Bookcase
Type a number: 4
Add any other furniture? y

Choose from the list below:
0: TV
1: Sofa
2: Table
3: Cabinet
4: Bookcase
Type a number: 0
Add any other furniture? y

Choose from the list below:
0: TV
1: Sofa
2: Table
3: Cabinet
4: Bookcase
Type a number: 0
Add any other furniture? n

Type m for metres or f for feet: m

Your room is 13.5 m³
Your Bookcase is 1 m³
Your TV is 0.2 m³
Your TV is 0.2 m³
You have 12.1 m³ of remaining volume
```