## tests

* Like regular unit test, doctests are considered ok if they compile and run without panic
* To demonstrate it runs as intended, use the macros from assert! family

```rust
let foo = "bar"
assert_eq!(foo, "bar");
```

[📒](https://doc.rust-lang.org/rustdoc/documentation-tests.html)