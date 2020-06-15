## Doc

```rust
/// Divides two numbers.
///
/// # Examples
///
/// <3 backtick here>
/// use dxp::div;
/// let result = div(10, 2);
/// assert_eq!(result, 5);
/// <3 backtick here>
///
/// # Panics
///
/// `div panics if the second argument is zero.
///
/// <3 backtick here>rust,should_panic
/// // panics on division by zero
/// use dxp::div;
/// div(10, 0);
/// <3 backtick here>
pub fn div(a: i32, b: i32) -> i32 {
    if b == 0 { panic!("Divide-by-zero error"); }
    a / b
}
```

[📒](https://doc.rust-lang.org/1.7.0/book/documentation.html) | 
[💻](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=3451c416fbc58ea406d3760465dd537e)