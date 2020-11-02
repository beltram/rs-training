## snippet tests handling Result

* it is possible to use the ? operator in doctests for when it's not useful to show complete error handling
* you'll have to declare a main function returning a Result to do so
* you may or may not hide this part

```rust
/// ```rust
/// use std::io;
/// # fn main() -> io::Result<()> {
/// let mut input = String::new();
/// io::stdin().read_line(&mut input)?;
/// # Ok(())
/// # }
/// ``` ```

[📒](https://doc.rust-lang.org/rustdoc/documentation-tests.html#using--in-doc-tests)