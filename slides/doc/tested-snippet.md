## testing your snippets

* Like regular unit test, doctests are considered ok if they compile and run without panic
* To demonstrate it runs as intended, use the macros from assert! family

```rust
/// # Example
/// ```rust
/// use your_crate::plus;
/// let a = 4;
/// let b = 5;
/// assert_eq!(a, 4);
/// assert_eq!(plus(a,b), 9);
/// ``` //end snippet   
pub fn plus(a: u32, b: u32) -> u32 { a + b }
```

[📒](https://doc.rust-lang.org/rustdoc/documentation-tests.html)