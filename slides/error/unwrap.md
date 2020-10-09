## unwrap

* aka unchecked error handling
* for Option & Result
* panics when None or Err
* use expect() to set a custom error or context message 

```rust
fn main() -> std::io::Result<()> {
    // thread 'main' panicked at 'called `Result::unwrap()` on an `Err` value: 
    // Os { code: 13, kind: PermissionDenied, message: "Permission denied" }',
    let _file = File::create("/foo.txt").unwrap();
    // thread 'main' panicked at 'Error from file creation: Os { code: 13, 
    // kind: PermissionDenied, message: "Permission denied" }'
    let _file = File::create("/foo.txt").expect("Error from file creation");
    Ok(())
}
```

[📒](https://doc.rust-lang.org/book/ch09-02-recoverable-errors-with-result.html#shortcuts-for-panic-on-error-unwrap-and-expect)