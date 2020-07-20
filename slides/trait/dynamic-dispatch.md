## dynamic dispatch

* or let's determine dispatch at runtime
* but we need a sized object anyway... 💡 a pointer is Sized

```rust
fn formulate(of: & dyn Formula) {}
// or a smart pointer such as Box
fn formulate(of: Box<dyn Formula>) {}

fn main() {
    let formula: u8 = 42;
    formulate(&formula as &Formula); // pass by casting
    formulate(&formula); // pass by coercing
}
```

* `-` less performant (slower virtual function calls)
* `-` no inlining
* `+` no copy of the function

[📒](https://doc.rust-lang.org/1.17.0/book/trait-objects.html#dynamic-dispatch)