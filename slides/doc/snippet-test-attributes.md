## snippet tests - attributes

* There are some annotation helping rustdoc do the right thing when testing doctests

```rust
/// ```should_panic     // Code should compile but not pass a tests
/// assert!(false);
/// ```.

/// ```compile_fail     // Compilation should fail. If it does not, test fails
/// let x = 5;
/// x += 2; // shouldn't compile!
/// ```.

/// ```no_run           // Code will be compiled but not run
/// loop { println!("Hello"); }  // useful when there is external dependencies
/// ```.

/// ```ignore           // Code will be ignored. You almost never want that
/// fn foo() {
/// ```.
```

[📒](https://doc.rust-lang.org/rustdoc/documentation-tests.html#attributes)