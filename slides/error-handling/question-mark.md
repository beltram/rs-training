## ? operator

* Can only be used on an Option or a Result in a function returning an Option or a Result respectively
* For Result, you can use the ? operator if applied on a function which return an Error which can be converted in the Error type declared in the function signature

```rust
fn main() -> Result<i32,io::Error> { // Work for main fuction since rust 1.26
    let mut file = File::open("file.txt")?; // can throw an io::Error
    let mut c = String::new();
    file.read_to_string(&mut contents)?; // can throw an io::Error
    Ok(c.trim().parse()?) // compile error
                    // ^ the trait `std::convert::From<std::num::ParseIntError>`
                    // is not implemented for `std::io::Error`
}
```

[📒](https://doc.rust-lang.org/edition-guide/rust-2018/error-handling-and-panics/the-question-mark-operator-for-easier-error-handling.html)