---
title: Testing
learning_intentions: ["Why testing your program is important", "How to fill in a testing table"]
success_criteria: ["Edit your first testing table"]
---

# Testing our programs

Testing software is really important. Having something that works as expected might be fine at first. However, what happens in situations where things don't go as expected? This means a program has bugs.

Bugs can cause real problems. In fact bugs in software can have [catastrophic consequences](https://www.pingdom.com/blog/10-historical-software-bugs-with-extreme-consequences/).

# What to test

Ultimately you need to test everything that can change the outcome of the program. At our current level, this really just means testing the program's…

	- inputs
	- calculations
    - conditions

When we test one aspect of the program we need to run a series of tests on it (not just one). These tests can be grouped into three categories:

	- expected cases
	- boundary cases
    - invalid cases

## Expected cases

Expected cases are things that we would typically think the user would do with the program. 

If the program is about checking if you are old enough to get into a bar, an expected test for the age that someone enters might be the value 24 or 11 or 67.

If the program was asking you to guess a random number between 1 and 100, an expected test for this program might be 50 or 94 or 3.

## Boundary cases

Boundary cases are those that are just on the limit of what we might expect (either just inside or just outside). Boundary case testing can be particularly useful when testing to see that conditions work as we want them to.

### Lower bounds

For a program asking if you are old enough to get into a bar, the lowest allowable age is the legal age to drink alcohol in New Zealand: 18. If you are younger than this, you will not be allowed into the bar.

Therefore, 18 is the lower bound. Your testing should also include 17 (just outside) and 19 (just inside), as these exist on either side of the boundary.

### Upper bounds

For a program asking that supplies a list of students for Room 10, when Room 10 only has 27 computers, then the list must only contain up to 27 students.

Therefore, 27 is the upper bound. Your testing should also include 28 students (just outside) and 26 students (just inside), as these exist on either side of the boundary.

## Invalid cases

Invalid cases can be trickier again. There are three main types of invalid test cases when it comes to user input:

- out of range values
- wrong type of data
- null values

### Out of range values

This invalid case is usually seen when there is an acceptable, expected range of values. The invalid cases are those that don't fit within that range. This is similar to boundary cases, except this type of testing is only concerned with those outside the bounds.

This can include:

- use list indices that are too high for the size of the list
- purchasing more items than are available in stock
- setting a person's age to a negative number

### Wrong type of data

This invalid case refers to data being in an unexpected type. For example, if you are asking for a user to enter an age as a number, and they enter the word 'fifteen', you cannot convert the string to an integer and thus the program would crash.

The four main types of data we deal with in this program are:

- numbers (integers, floats)
- strings
- boolean values (True, False)
- collections (lists, dictionaries)

### Null values

This invalid case refers to instances where no data was provided. This often occurs when a program uses ``input()`` to ask for data but the user presses Enter without typing anything.

# Testing table

You should always document your testing to keep track of what you have fixed and what needs fixing. There are many ways to document testing but here is a way that we have found works well at school. A **testing table** like this helps us plan what we need to test to ensure we test thoroughly.

Again let's use the bar entry age checker to create a testing plan:

| Input / Type of test  | Value(s) to enter | Expected result | Actual result |  Comments/changes needed |
| :-- | :-- | :-- | :-- | :-- |
| age (E) | 23 | You may enter | *Screenshot or copy-paste of the console text here* | *If we need changes, we note them here and run the test again* |
| age (E) | 10 | You are too young to enter | You may enter | Didn't work. Need to fix my if statement |
| age (E) | 10 | You are too young to enter | You are too young to enter | |
| age (B) | 18 | You may enter | You may enter | |
| age (B) | 17 | You are too young to enter | You are too young to enter | |
| age (B) | 19 | You may enter | You may enter | |
| age (I) | "banana" | Please enter a number | Program crashed | I need to use try/except |
| age (I) | "banana" | Please enter a number | Please enter a number | |
| age (I) | null | Please enter a number | Please enter a number | |

You will be provided with a testing table as part of your assignment. You must fill it in with the tests you will carry out.

A copy of the testing table document can be found on [Teams → 11DIT → General → Files → Assessment → AS91883 Testing Table.docx](https://onslowcollege.sharepoint.com/:w:/s/11DIT499/EdGUoaEYHq1FgklSh30Ka-UBo1Kvgww3rByGKQeDBNKCMQ?e=0gnw6S).