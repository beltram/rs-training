## many mutable borrow

* a variable can only be mutably borrowed ONCE

```rust
let mut beltram = String::from("Beltram");
let mut alias = &mut beltram;
//              ------------ first mutable borrow occurs here
println!("Hello {}", &mut beltram);
//                   ^^^^^^^^^^^^ second mutable borrow occurs here
println!("Hello {}", alias);
//                   ----- first borrow later used here
```