## macros

* a way of writing code that writes other code
* the code is executed before the compiler interprets the code (e.g. allows trait implementation)
* a macro is able to take a variable number of parameters 
```rust
println!("Hello");
println!("Hello {}", name);
```
* a macro is able to implement a trait for a given type
* a macro is more complex to write than a simple function
[📒](https://doc.rust-lang.org/book/ch19-06-macros.html)
 