## closure scope

* one can borrow or own local variables in a closure
* by default, Rust borrows local variables
* but if required, it takes ownership of local variables

```rust
let greeting = String::from("Hello ");
// greeting is borrowed here
let welcome = |it: &str| println!("{}{}", greeting, it);
// get_greeting takes ownership of greeting because it requires to
let get_greeting = || greeting;
```

[📒](https://doc.rust-lang.org/1.17.0/book/closures.html#closures-and-their-environment)