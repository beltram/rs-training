## Propagating error

* For propagating error, rust has a sugar syntax. The ? operator
* If an Option has Some(value) or a Result Ok(value) the value inside will be passed to next step
* If an Option has None or a Result Err(e) will return them immediately to the caller of the function

```rust
fn read_username_from_file() -> Result<String, io::Error> {
    let f = File::open("username.txt")?;
    // Can be desugar as:
    let f = File::open("username.txt"); 
    let f = match f {
        Ok(file) => file,
        Err(e) => return Err(e),
    };
```