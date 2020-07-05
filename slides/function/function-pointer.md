## function pointer

* rare syntax
* does not work with dynamic dispatch ie no generics

```rust
fn plus_one(input: u8) -> u8 { input + 1 }
fn anonymous_function(input: u8, func: fn(u8) -> u8) -> u8 { func(input) }
fn main() {
    // everything is an expression
    let incrementer = plus_one; // so can be assigned to a variable
    let incrementer: fn(u8) -> u8 = plus_one; // with explicit type
    let three = incrementer(2);
    let four = anonymous_function(3, incrementer); // reuse
    let nine = anonymous_function(3, |i| i * i); // accepts a closure
}
```

[📒](https://doc.rust-lang.org/1.7.0/book/functions.html#function-pointers)