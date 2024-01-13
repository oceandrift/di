# oceandrift/di

A lightweight **Dependency Injection (DI)** framework with focus on simplicity.

## Installation

When using DUB, it’s as simple as running `dub add oceandrift-di`.

## Usage

See in-code documentation for details.
Or check out the [pre-rendered copy](https://oceandrift-di.dpldocs.info/oceandrift.di.html)
on dpldocs.

```d
class Dependency { }

class Foo {
    this(Dependency d) {
        // …
    }
}

// Instantiate DI.
// Then let it resolve the whole dependency tree
// and construct dependencies as needed.
auto di = new DI();
Foo foo = di.resolve!Foo();
```
