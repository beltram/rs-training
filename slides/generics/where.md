## where clause

* prefer for long bounds

```rust
fn print_human<T>(of: T) where
    T: Human + Display {
    println!("{}", of)
}

fn father<T, F>(of: T) -> Vec<(F, M)> where
    T: Human,
    F: Human {}

// this couldn't have been expressed without 'where'
impl<T> Human for T where
    Option<T>: Display {
    fn maybe_print(self) { println!("{}", Some(self)); }
}
```

[📒](https://doc.rust-lang.org/stable/rust-by-example/generics/bounds.html)