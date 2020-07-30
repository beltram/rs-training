## Unwrap

* If an Option has Some(value) or a Result Ok(value) unwrap() will return the value
* If an Option has None or a Result Err(e) will panic. For Err, the e value will be used as error message
* You can also use expect() which is doing the same thing but let you set a custom error or context message 

```rust
use std::fs::File;

fn main() -> std::io::Result<()> {
// thread 'main' panicked at 'called `Result::unwrap()` on an `Err` value: 
// Os { code: 13, kind: PermissionDenied, message: "Permission denied" }',
// src/main.rs:4:17
    let _file = File::create("/foo.txt").unwrap();
// thread 'main' panicked at 'Error from file creation: Os { code: 13, 
// kind: PermissionDenied, message: "Permission denied" }', src/main.rs:5:17
    let _file = File::create("/foo.txt").expect("Error from file creation");
    Ok(())
}
```

[📒](https://doc.rust-lang.org/book/ch09-02-recoverable-errors-with-result.html#shortcuts-for-panic-on-error-unwrap-and-expect)