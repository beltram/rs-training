## lifetime declaration

* declare with single quote ' followed by a name (prefer single letter starting with 'a')
* by default lifetime 'l is implicitly declared on borrows
* in Pascal notation, declare after & and separate from type with a space
* declare locally on a function after its name (same spot for generics)

```rust
fn trim_after<'a>(from: &'a str, prefix: &str) -> &'a str {
    // ...              ^^^                       ^^^
    // because we return a borrow of 'from' and not 'prefix'
    // we don't care about 'prefix' lifetime because we don't return/borrow it
    // but we could have assign it one lifetime explicitly
    &from[idx..]
}
fn reusing_lifetimes<'a>(x: &'a str, y: &'a str, z: &'a str) {}
fn many_lifetimes<'a, 'b, 'c>() {}
fn lifetimes_and_generics<'a, 'b, T, V>() {}
// order matters ! lifetimes then generics
```