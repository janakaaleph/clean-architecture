# Reactive MVVM

\[Work in Progress\]

Everything is a signal!

## ViewModel Template

```
// Dependent UseCases via constructor injection

// Inputs - Some public mutable reactive properties

// Transformations - Any logic that must happen in-between inputs and outputs

// Outputs - Some public observable but immutable properties

/* Notice that only inputs and outputs can be public. Everything else should be an implementation detail, and thus private. */

```