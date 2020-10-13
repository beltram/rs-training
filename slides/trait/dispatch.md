## dispatch

* rustc needs to know the size of every object in order to allocate stack frame memory

```rust
trait Formula {}
impl Formula for String {}
impl Formula for u8 {}

fn formulate(of: Formula) {} // compilation error
```

* here 'of' can either be 'u8' (1 byte) or 'String' (24 bytes)
* rustc needs to determine which implementation of a trait is actually run
* let's call this 'dispatch'

[📒](https://doc.rust-lang.org/1.17.0/book/trait-objects.html#trait-objects)