## standard enum

* Option and Result are enums which are in the standard library and widely used

```Rust
pub enum Option<T> { // rust solution to eliminate null values
    None,
    Some(T),
}

pub enum Result<T, E> { // rust standard error handling
    Ok(T),
    Err(E),
}
```

[📒](https://doc.rust-lang.org/book/ch06-01-defining-an-enum.html#the-option-enum-and-its-advantages-over-null-values)