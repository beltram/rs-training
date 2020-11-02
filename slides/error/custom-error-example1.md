## custom Error type

```rust
// defines a custom Error type and implements a conversion from another Error
#[derive(Debug)] // mandatory to be able to use the ? operator
struct AppError {
    kind: String,
    message: String,
}

impl From<io::Error> for AppError { // enables conversion
    fn from(error: io::Error) -> Self {
        AppError {
            kind: String::from("io"),
            message: error.to_string(),
        }
    }
}
```

[💻](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=2c779817f9bd6c4a179ab43779c963ef)