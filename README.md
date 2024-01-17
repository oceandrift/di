# oceandrift/di

A lightweight **Dependency Injection (DI)** framework with focus on simplicity.

- Inversion of Control (IoC).
- Convention over configuration.
- Injects dependencies via constructor parameters.
- Supports structs as well (… as classes and interfaces).
- No clutter – this library is a single, readily comprehensible file.
- No external dependencies. (\*Only the D standard library is used.)

## Installation

When using DUB, it’s as simple as running `dub add oceandrift-di`.

## Usage

See in-code documentation for details.
Or check out the [pre-rendered copy](https://oceandrift-di.dpldocs.info/oceandrift.di.html)
on dpldocs.

```d
class Dependency {}

class Foo {
    this(Dependency d) {
        // …
    }
}

// Bootstrap the DI framework.
// Then let it resolve the whole dependency tree of `Foo`
// and construct dependencies as needed.
auto di = new DI();
Foo foo = di.resolve!Foo();
```
