---
title: Regular vs Context-Free
grand_parent: 13DTC
parent: L3 Computer Science
nav_order: "ad"
---

<iframe width="560" height="315" src="https://www.youtube.com/embed/5lXAjh4mdnY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


# Regular

A **regular** language can be defined by a regular expression. A regular language is a context-free language, but not all context-free languages are regular languages.

Regular expressions themselves define all valid strings within a language. For example, the regex ``[A-Z]{3}[0-9]{3}`` describes all possible valid strings (AAA000, AAA001, AAA002, etc.); this collection of strings form the language.

Regular expressions are always evaluated in order, either left-to-right or right-to-left. So, the above example always generates three letters followed by three digits; there is no ambiguity to the order.

Even with metacharacters such as ``.`` (representing any character) or ``*``/``?`` (representing one or none-to-many of a character or expression), these are evaluated in order. Therefore, for the regex ``[A-Z]{3}.{3}``, ABC!@# is valid within the language but !@#ABC can never be.

Therefore, the production rules for a regular language are restricted in the following way:

- a single non-terminal character at the left must transform to:
  - a single terminal character, or
  - a single terminal character followed/preceded by (but not both in the same language) a single non-terminal character

``A → cB``, ``A → c``, ``A → є`` (this symbol means 'none')

# Context-Free

A **context-free** language can be defined by a context-free grammar. A regular language is a context-free language, but not all context-free languages are regular languages.

The major difference is that while regular expressions are always evaluated in order from left-to-right (or right-to-left), context-free grammars can be a bit more ambiguous. Non-terminal characters can transform to other non-terminal characters in any configuration.

Specifically, "context-free" means that a non-terminal character can transform regardless of its *context* (the characters that surround it). Therefore, a rule such as ``A -> B`` (non-terminal to non-terminal) is possible — A can become B, regardless of any non-terminals. Therefore, these are all possible:

- ``A -> B``
- ``xA -> xB``
- ``xyzAxyz -> xyzBxyz``
- ``Aflyingmonkeys -> Bflyingmonkeys``

The flexibility of context-free languages implies that context-free languages have memory: characters can be stored and retrieved again later as a non-terminal character, making them effectively variables.

In this way, a context-free grammar can parse something like a palindrome: a word or phrase that is spelt the same in one direction as the other. For example, "bob", "12321", or even the phrase "rats live on no evil star". A regular language cannot handle this since it parses only in one direction — it cannot go "back" to inspect a previous character, therefore is unable to detect whether the characters at each end match.