---
title: Testing Task
---

# Task

> **Filename**: facts.py

Create a program that displays a menu with facts on a topic of your choice.

**Before you start programming**, you must fill in a copy of the [testing table](https://onslowcollege.sharepoint.com/:w:/s/11DIT499/EdGUoaEYHq1FgklSh30Ka-UBo1Kvgww3rByGKQeDBNKCMQ?e=0gnw6S) with input values for [expected cases](testing.md#expected-cases), [boundary cases](testing.md#boundary-cases), and [invalid cases](testing.md#invalid-cases). This will be uploaded as part of the assignment.

## Testing requirements

As you write the program code, test the program according to your testing table.

If your one of your tests fails:

- add a comment explaining what you think went wrong and what you will change
- add a new row below the current row
- copy and paste the test to the new row
- make changes to the code
- test again

**DO NOT** leave the testing table until you have made the program fully functional. A testing table that shows no issues would be very suspicious and give your teachers grounds to doubt that:

- you did any testing, or
- you wrote your own code

## Program requirements

Each menu item contains:

- a number
- a single word that summarises a fact

When the user types in a number corresponding to a menu item, the fact is shown on-screen in full.

The program should continue until the user types Q to quit.

## Expected output

```
Welcome to Cat Facts
Please type a number to see a fact

===========
1) Whiskers
2) Tails
3) Night-vision
4) Falling
5) Egypt
===========
Q) Quit
===========

Please type a number: 6
Please enter a number between 1 and 5.

Please type a number: 5
Did you know? Cats were revered in ancient Egypt.
There are even some gods depicted as having cat heads,
such as Mafdet, Bastet, Sekhmet, and Mut.
```