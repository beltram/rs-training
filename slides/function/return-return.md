## return keyword

```rust
fn return_keyword() -> u8 { 
    // not recommended
    // prefer semicolon absence
    return 42 
}
fn except_for_early_return() -> u8 { 
    return 42; // you can use return with semicolon
    let a = 1 + 1; // this will never be reached
}
```

[📒](https://doc.rust-lang.org/1.7.0/book/functions.html)