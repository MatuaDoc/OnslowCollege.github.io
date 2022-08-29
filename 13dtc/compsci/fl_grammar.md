---
title: Formal Grammars & Parsing
grand_parent: 13DTC
parent: L3 Computer Science
nav_order: "ac"
---

# What is a formal grammar?

{% include shout.html side="left" emote="📓" markdown="As with spoken and written languages, formal languages contain a **grammar** that describes the rules of the language — what constitutes valid input. The grammar describes how the language's **alphabet**, or list of the smallest inputs that might trigger a transition." %}

For example, in the [number parsing task](fl_fsm#task-2) in [Finite State Machines](fl_fsm), the alphabet was:

| --- | --- | --- | --- | --- | --- |
| 0 | 1 | 2 | 3 | 4 | 5 |
| 6 | 7 | 8 | 9 | . |   |

By joining these characters in various ways, you can create valid numbers according to the rules of our finite state machine.

## What's in a grammar?

The alphabet in a formal language is manipulated according to the language's rules, the grammar. A grammar consists of:

1. a finite alphabet, or list of acceptable strings, called ``∑`` (sigma). The alphabet can be letters, numbers, symbols, or even words.
2. a finite set of non-terminal symbols, called ``N``. These symbols are acceptable input but will not figure in the output.
3. a start symbol called ``S``. It is also a non-terminal symbol, but we treat it separately.
4. a finite set of rules, called ``R``.  Rules accept a left-hand side (LHS), which starts with ``S``, that is transformed to a result called the right-hand side (RHS).
    - If the RHS contains non-terminal symbols (from ``N``), it becomes the LHS for another rule. These rules are applied **recursively**.
    - If the RHS contains only symbols from ``∑``, the input is valid and the RHS is the output.

## Example 1: currency string builder

For example, let's add a new feature to our number parser: let's add a currency symbol (``$``, dollar sign) to the front.

The number parser has the following rules:

- it is a number only if it contains 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, a decimal point, or a dollar sign
- there can only be one (1) decimal point or none at all
- the decimal point must have numbers on either side
- there can be any number of digits before the decimal point
- there must only be two (2) digits after the decimal point
- there must be one (1) dollar sign at the front of the input

These rules are expressible with the following grammar:

- ``∑`` is ``{0, 1, 2, 3, 4, 5, 6, 7, 8, 9, ., $}``
- ``N`` is ``{CURR, NUMBER, DIGIT}``
  - ``CURR`` represents our start symbol
  - ``NUMBER`` represents any string of numbers
  - ``DIGIT`` represents a single digit
- ``R`` is:
    1. ``CURR -> $ NUMBER . DIGIT DIGIT``
    2. ``NUMBER -> DIGIT``
    3. ``NUMBER -> DIGIT NUMBER``
    4. ``DIGIT -> 0``
    5. ``DIGIT -> 1``
    6. ``DIGIT -> 2``
    7. ``DIGIT -> 3``
    8. ``DIGIT -> 4``
    9. ``DIGIT -> 5``
    10. ``DIGIT -> 6``
    11. ``DIGIT -> 7``
    12. ``DIGIT -> 8``
    13. ``DIGIT -> 9``

Let's examine each piece in detail.

### ∑: the alphabet

{% include shout.html side="left" emote="∑" markdown="This is the alphabet or list of valid characters/words. Not only are these the only allowed characters/words, these are the only valid output resulting from ``R``." %}

### N: the non-terminal symbols

{% include shout.html side="left" emote="N" markdown="These are the non-terminal symbols. Each of these symbols represents a placeholder within the string as the input is transformed by ``R``. None of them are part of ``∑``, so none of them is part of a valid output." %}

### S: the start symbol

{% include shout.html side="left" emote="S" markdown="In this case, ``S`` is represented by ``CURR`` — this is the whole input string, hence why it's the start symbol — we begin with this input, parse it, validate it, and output it." %}

### R: the rules

{% include shout.html side="left" emote="R" markdown="Each of these rules tells us how to transform the input at each stage in the process. For example, rule 1 tells us that ``CURR`` LHS should be transformable to ``$ NUMBER . DIGIT DIGIT`` RHS." %}

For instance, given a string ``$2.34``, the rules could be applied like so:

1. rule 1
    - rule: ``CURR -> $ NUMBER . DIGIT DIGIT``
    - output: ``$ NUMBER . DIGIT DIGIT``
    - because this is the start, therefore we use ``CURR`` which is our ``S``. There is only one rule that can be applied to ``CURR``, which is rule 1.
2. rule 2
    - rule: ``NUMBER -> DIGIT``
    - output: ``$ DIGIT . DIGIT DIGIT``
    - because ``NUMBER`` is the only non-terminal symbol (from ``N``) left to parse; the applicable rule is 2, since there is only one digit between the dollar sign and the decimal point.
3. rule 6 
    - rule: ``DIGIT -> 2``
    - output: ``$ 2 . DIGIT DIGIT``
4. rule 7
    - rule: ``DIGIT -> 3``
    - output: ``$ 2 . 3 DIGIT``
5. rule 8
    - rule: ``DIGIT -> 4``
    - output: ``$ 2 . 3 4``

Because no more rules can be applied, the input is considered valid according to the grammar — the output is ``$2.34``, same as the input.

# Task 1: 1 to A, 2 to B

Create a state transition table for an FSM that can transform integer numbers from numbers to letters and vice-versa.

- each digit ``N`` is transformable to the letter at ``N`` position in the alphabet. For instance, ``1`` is ``A``, ``2`` is ``B``, etc.
  - ``0`` is transformable to ``J``
- on the other hand, each letter is transformable back to the number value. For instance, ``C`` is ``3``, ``D`` is ``4``, etc.
- letters can only be upper cased
- input can contain a mix of numbers and letters
- the string can be any length

Here are some examples of valid inputs:

| Valid | Reason for validity |
| :-: | :-- |
| ``1`` | Contains a digit, which will transform to ``a`` |
| ``A`` | Contains a letter, which will transform to ``1`` |
| ``BABE`` | Contains letters which will transform to ``2125`` |
| ``0145`` | Contains digits which will transform to ``JADE`` |
| ``43EGA6`` | Contains a mixture of digits and letters which will transform to ``DC571F`` |

And here are some invalid inputs:

| Invalid | Reason for invalidity |
| :-: | :-- |
| ``0.1`` | ``.`` cannot be transformed |
| ``XYZ`` | These letters cannot be transformed |
| ``abc`` | Letters must be upper cased |

# Task 2: grammar table

Based on your understanding of how this FSM works, let's define the formal language to express the rules for determining if input is valid and what the output should be.

In groups, fill out this table (in a Word document or on paper) then fill out the details for the language's alphabet and formal grammar:

| | | |
| :-- | :-- | --: |
| **∑** | alphabet | |
| **N** | non-terminal symbols | |
| **S** | start symbol | |
| **R** | rules | |