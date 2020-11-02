## testing your snippets

* like regular unit test, doctests are considered ok if they compile and run without panic
* use macros from 'assert!' family to demonstrate it runs as intended

```rust
/// # Example
/// ```rust
/// use your_crate::plus;
/// let a = 4;
/// let b = 5;
/// assert_eq!(a, 4);
/// assert_eq!(plus(a,b), 9);
/// ``` //(escape reveal.js)   
pub fn plus(a: u32, b: u32) -> u32 { a + b }
```

[📒](https://doc.rust-lang.org/rustdoc/documentation-tests.html)