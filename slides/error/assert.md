## assert macro panics

* assert macro family let you use a test assertion to decide whether to panic or not
* often used in tests, but can also be useful in production code or for debugging

```rust
fn main() {
    assert!(boolean); // will panic if boolean is false
    assert_eq!(a, b); // will panic if a != b
    assert_ne!(a, b); // will panic if a == b
    assert_eq!(a, b, "a and b should be equal"); // panic with an error message
    // note that debug_assert!(), debug_assert_eq!(), debug_assert_ne!() macros
    // exist but will be omitted when using release profile
}
```

[📒](https://doc.rust-lang.org/1.17.0/book/error-handling.html#the-basics)