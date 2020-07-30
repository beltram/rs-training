# Panicking

* Panic means that the program will stop throwing an error
* Panic is the most basic way to (not) handle error in rust
* You can use panic!() macro for unrecoverable errors 
* panic! don't leak memory

```rust
fn main() {
    panic!(); //thread 'main' panicked at 'explicit panic', src/main.rs:2:5
    let x = 2.2;
    //thread 'main' panicked at '2.2 is not an integer', src/main.rs:5:5
    panic!("{} is not an integer", x);
}
```

[📒](https://doc.rust-lang.org/1.17.0/book/error-handling.html#the-basics)