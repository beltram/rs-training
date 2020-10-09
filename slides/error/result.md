## Result

* should be used as return type for a function where we need to handle errors.
* is annotated with the #[must_use] attribute : if a result value is ignored you get a compiler warning

```rust
// Result can be seen as the following type Result<Value, Error>
fn is_old(boomer: u8) -> Result<u8, String> { // Error type can be very simple
// Here we are using a simple if to handle the 2 arms, but a match expression
// could be used as well. Especially if you have several Ok(value)
    if boomer < 60 { Err("Still young".to_string()) }
    else { Ok(boomer) }
}
fn main() {
    let age_category: Result<u8, String> = is_old(50);
    match age_category { // All the Result variant must be handled
        Ok(_) => println!("Not that young anymore"),
        Err(e) => println!("{}", e), // Will print: Still young
    }
}
```
[📒](https://doc.rust-lang.org/std/option/index.html)