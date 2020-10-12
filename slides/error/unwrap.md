## .unwrap()

* not recommended !
* aka unchecked error handling
* for Option & Result
* panics when None or Err
* use expect() to set a custom error or context message 

```rust
fn main() -> std::io::Result<()> {
    // panicked at: Os { kind: PermissionDenied, message: "Permission denied" }',
    let _file = File::create("/foo.txt").unwrap();
    // panicked at 'Error from file creation: Os { kind: PermissionDenied, message: "Permission denied" }'
    let _file = File::create("/foo.txt").expect("Error from file creation");
    Ok(())
}
```

[📒](https://doc.rust-lang.org/book/ch09-02-recoverable-errors-with-result.html#shortcuts-for-panic-on-error-unwrap-and-expect)