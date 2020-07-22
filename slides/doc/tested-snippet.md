## testing your snippets

* Like regular unit test, doctests are considered ok if they compile and run without panic
* To demonstrate it runs as intended, use the macros from assert! family

```rust
/// ```rust
/// use your_crate::plus; // import the function to test
/// let a = 4;
/// let b = 5;
/// assert_eq!(a, 4);
/// assert_eq!(plus(a, b), 9);
/// ``` ``` 

[📒](https://doc.rust-lang.org/rustdoc/documentation-tests.html)