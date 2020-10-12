## error propagation

* for propagating errors, use the ? operator
* if Some(value) or Ok(value), the value inside will be passed to next step
* if None or Err(e), early aborts the function and returns the Option or Result

```rust
fn read_username_from_file() -> Result<String, io::Error> {
    let f = File::open("username.txt")?;
    // Can be desugared as:
    let f = File::open("username.txt"); 
    let f = match f {
        Ok(file) => file,
        Err(e) => return Err(e),
    };
```