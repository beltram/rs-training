## Unwrap

* For Result you have the unwrap_err and expect_err functions
* For Option and Result you have some more advanced functions that let you define some fallback behavior

```rust
fn main() {
    let ok: Result<i8, &str> = Ok(8);
    let ko: Result<i8, &str> = Err("ko value");
    ok.unwrap_err(); // will panic (opposite behavior than unwrap())
    ko.unwrap_err(); // will return "ko value"
// In case of None or Err, take the given value. Value must match with the
// inner type of the Option/Result
    ko.unwrap_or(5); 
// In case of None or Err, take the default value of the inner type
    ko.unwrap_or_default();
// Similar to unwrap_or but take a closure instead of a value. Function
// return type must match.
    ko.unwrap_or_else(|_| 2 * 4); // variable in the closure is the value of Err
}
```

[📒](https://doc.rust-lang.org/book/ch09-02-recoverable-errors-with-result.html#shortcuts-for-panic-on-error-unwrap-and-expect)