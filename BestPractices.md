# Best practices
Guidance for what to ideally avoid. These are not
hard set rules and should be broken when needed, but
should ideally be followed.

## Application level
### Safety critical
Security critical is defined [here](https://en.wikipedia.org/wiki/Safety-critical_system).
tl;dr is defined as software that needs to do something **right**
or else **very very** bad things could happen i.e. human life at risk.

#### 1. Avoid recursion
Recursion is a great tool, but it also means it is
harder to track and trace bugs within them. Prefer
loops to recursion.

## Languages

### Rust
#### 1. Avoid unwrap
The `unwrap()` method should be avoided.
In safety critical applications, a race car for
example, we should handle all errors. Using `unwrap`
throws a [panic](https://doc.rust-lang.org/std/macro.panic.html)
and crashes the program. Alternatives include `unwrap_or()` or `unwrap_or_else()`.

#### 2. Composition over inheritance
Prefer composing objects rather than inheriting them.
Rust does not have a clean way of creating an 
inheritance system and encourages you to use
composition instead.
