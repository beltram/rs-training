## ? operator

* can only be used on an Option or a Result
* enclosing block MUST return Option or Result respectively

```rust
fn main() -> Result<i32, io::Error> { // works for main function since Rust 1.26
    let mut file = File::open("file.txt")?; // may throw an io::Error
    let mut c = String::new();
    file.read_to_string(&mut c)?; // may throw an io::Error
    Ok(c.trim().parse()?) // compile error
    // ^ the trait `From<ParseIntError>` is not implemented for `io::Error`
}
```

* ? is only applicable when Err is convertible to enclosing Err
* ? prints out a debug representation of Err(e)

[📒](https://doc.rust-lang.org/edition-guide/rust-2018/error-handling-and-panics/the-question-mark-operator-for-easier-error-handling.html)