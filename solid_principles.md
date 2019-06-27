# SOLID Principles

## [S]ingle Responsibility

Every object should have a single responsibility. Each responsibility should be encapsulated by it’s class There should never be more than one reason for a class to change. More responsibilities imply more likelihood of changes. There are two aspects that we need to strive in Single Responsibility principle:

- Cohesion - How strongly related and focused are the various responsibilities of a module
- Coupling - The degree to which each program module relies on each one of the other modules.

We should strive to achieve High cohesion and Low coupling.

## [O]pen Closed Principle

Open/Close principle states that Software entities such as Classes, Modules and functions should be Open for extension, but Close for modification.

- Open for Extension: New behavior can be added in future
- Close for modification: Changes to source code is not required or minimal if required.

Best way of achieving this goal is to use Abstraction. Fundamentally a transfer service is moving money from A to B, so this can be abstracted. We would rarely need to modify it afterwards. Implementation wise, different transaction types may be different. So we can extend transaction core implementation, without modifying it.

## [L]iskov Substitution Principle

Any derived class should be substitutable by any other derived class. For the most part most modern day IDE/Compilers will handle this. A more subtle point is that pre-conditions can only get weaker, while post conditions can only get stronger.

Transaction value precondition that it should be positive, but if we make the precondition stronger by saying value should be > 100, then substitution will break because all those derived classes that used 0-99 will break.

Post condition is that transaction was success or fail only. If we weaken the post condition by saying there is a new state success, unknown, fail. Then substitution will fail because consumers won’t know how to deal with new state. However if we said transactions are guaranteed to succeed (post condition is stronger) things will still be ok because substitution will still work.

## [I]nterface Segregation

Don’t force clients to implement interfaces they don’t need. Composition over inheritance.

\[Work In Progress\]

- Add more description, example

## [D]ependency Inversion Principle

1. High-level modules should not depend on low-level modules. Both should depend on abstractions.
1. Abstractions should not depend on details. Details should depend on abstractions.

\[Work In Progress\]

- Add more description, example
