# Classes I: Protocols

## Learning intentions

You will learn:

- what a protocol is
- when to use a protocol
- how to declare a protocol class
- how to declare that a class conforms to a protocol

### Success criteria

You will know that you have completed the learning when:

- you have declared a protocol class
- you have declared at least two classes that conform to the protocol

# What is a protocol?

**Protocols** allow you to define a set of methods inside a *protocol class*. These methods are only declared; they contain no implementation. For example:

```python
from typing import Protocol

class HonkProtocol(Protocol):
	def honk() -> None:
		pass
```

Above, we have declared a protocol class called ``HonkProtocol``. Within that, we have also declared a method called ``honk()``. This method doesn't currently do anything.

However, we then create another class *conforms* to the protocol.

```python
class Goose():
	def honk() -> None:
		print("Honk!")
```

Because the ``Goose`` class contains same declaration for a method called ``honk()``, we know that ``Goose`` conforms to ``HonkProtocol``.

Let's add another class that conforms to ``HonkProtocol``.

```python
class Motorcar():
	def honk() -> None:
		print("Beep!")
```

As you can see, ``Motorcar`` declares the same ``honk()`` method but has a different implementation. Instead of printing "Honk!", it prints "Beep!". However, the implementation is irrelevant — the important thing is that both classes contain the appropriate method. Therefore, you can do this:

```python
my_goose = Goose()
my_car = Motorcar()

my_honking_things = [my_goose, my_car]

for thing in my_honking_things:
	thing.honk()

# Honk!
# Beep!
```

## More complex protocols

A more useful protocol would be one that defines a method that returns a value. The protocol can act as a guarantee that:

- the method **must** return a value
- the method **must** return the same type, no matter what each conformant class' implementation does

This is very useful if you have a collection of instances of different classes but want to perform the same task for all of them. For instance, let's add a ``weight()`` function to ``HonkProtocol`` — it will guarantee that:

- anything that can honk **must** weight something
- the weight of anything that can honk **must** be measurable as a ``float``

```python
from typing import Protocol

class HonkProtocol(Protocol):
	def honk() -> None:
		pass

	def weight() -> float:
		pass

class Goose():
	def honk() -> None:
		print("Honk!")

	def weight() -> float:
		return 1.7 #kg

class Motorcar():
	def honk() -> None:
		print("Beep!")

	def weight() -> float:
		return 1524.0 #kg
```

Because we can guarantee that both ``Goose`` and ``Motorcar`` will produce output of the same type, ``float``, and their method definitions match that given in ``HonkProtocol`` exactly, we can be confident about doing things like the following:

```python
total_weight = 0.0
for thing in my_honking_things:
	total_weight = total_weight + thing.weight()
	thing.honk()

print(total_weight + " kg")

# Honk!
# Beep!
# 1523.7 kg
```

# Task

Now it's your turn to create properties in a class!

1. [Accept this Github Classroom assignment](#task)
2. Open the repository in Visual Studio Code ([instructions here](../../Classroom/README.md))
3. Edit the code to pass the tests
4. Commit and push your code to Github for autograding
