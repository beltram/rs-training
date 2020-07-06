## return type

```rust
// rust has no return type inference, return type has to be declared explicitly
fn explicit_return_type() -> u8 {
    42 // no semicolon ; implicit return
}
fn void_return_type() -> () {
    println!("statement terminated by semicolon ;");
}
fn implicit_void_return() { 
    println!("explicit void will be caught by clippy"); 
}
```

[📒](https://doc.rust-lang.org/1.17.0/book/functions.html)