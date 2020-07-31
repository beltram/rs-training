## Custom Error Type

```rust
// Defining a custom Error type and implements a conversion from another Error
#[derive(Debug)]     // Mandatory to be able to use the ? operator
struct AppError {
    kind: String,    // type of the error
    message: String, // error message
}
// Implement std::convert::From for AppError; from io::Error
impl From<io::Error> for AppError {
    fn from(error: io::Error) -> Self {
        AppError {
            kind: String::from("io"),
            message: error.to_string(),
        }
    }
}
```

[💻](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=2c779817f9bd6c4a179ab43779c963ef)