## standard enum

* Option and Result are enums which are in the standard library and widely used
* we'll cover both later on <a href="#/14/3">here</a>

```Rust
pub enum Option<T> { // for dealing with absence
    Some(T),
    None,
}

pub enum Result<T, E> { // for error handling
    Ok(T),
    Err(E),
}
```

[📒](https://doc.rust-lang.org/book/ch06-01-defining-an-enum.html#the-option-enum-and-its-advantages-over-null-values)