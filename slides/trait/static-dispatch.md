## static dispatch

* generate at compile time specialized variants of formulate
* use a generic bound to perform static dispatch
* this is called 'monomorphization'

```rust
fn formulate<T: Formula>(of: T) {}

// rustc will generate those:
// fn formulate(of: String) {}
// fn formulate(of: u8) {}
```

* `+` recommended, more performant most of the time
* `+` allows inlining the function
* `-` may generate a lot of copies of the function

[📒](https://doc.rust-lang.org/1.17.0/book/trait-objects.html#static-dispatch)