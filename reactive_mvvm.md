# Reactive MVVM

\[Work in Progress\]

Everything is a signal!

## ViewModel  Responsibilities

* Hold UI related data for the view layer

* Allow sharing of data between views

* Restore lightweight data after system-initiated process death

* Handle asynchronous input from view layer reactively

* Composite and orchestrate execution of UseCases

* Handle UseCase status such as success and error state

* Transform UseCase output to observable output that will be observed by view layer





## ViewModel Template

```
// Dependent UseCases via constructor injection

// Inputs - Some public mutable reactive properties

// Transformations - Any logic that must happen in-between inputs and outputs

// Outputs - Some public observable but immutable properties

/* Notice that only inputs and outputs can be public. Everything else should be an implementation detail, and thus private. */

```