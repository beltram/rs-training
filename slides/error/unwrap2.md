## unwrap

* Result adds 'unwrap_err' and 'expect_err'
* Option & Result you have advanced operators to define some fallback behavior

```rust
let ok: Result<i8, &str> = Ok(8);
let ko: Result<i8, &str> = Err("ko value");
ok.unwrap_err(); // panics !!! (opposite of unwrap())
ko.unwrap_err(); // will return "ko value"
ko.unwrap_or(5); // when None or Err, returns fallback (5 here) 
ko.unwrap_or_default(); // when None or Err, returns T::default()
ko.unwrap_or_else(|e| 2 * 4); // 'e' is the value of Err
```

[📒](https://doc.rust-lang.org/book/ch09-02-recoverable-errors-with-result.html#shortcuts-for-panic-on-error-unwrap-and-expect)