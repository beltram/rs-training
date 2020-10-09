## panic!

* unrecoverable error
* upon panic programm stops and throws an error
* basic way (not) to handle error in rust === unchecked exception for jvm e.g. RuntimeException 
* you can use panic!() macro for unrecoverable errors 
* panic! doesn't leak memory (all memory is garbaged)

```rust
fn main() {
    //thread 'main' panicked at 'because I want to fail'
    panic!("because I want to fail");
}
```

[📒](https://doc.rust-lang.org/1.17.0/book/error-handling.html#the-basics)