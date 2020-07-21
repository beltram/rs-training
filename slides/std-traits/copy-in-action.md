## [Copy](https://doc.rust-lang.org/std/marker/trait.Copy.html) in action

* usage of copy is always implicit

```rust
let forty_two: u8 = 42;
//             ^ u8 implements Copy
let the_answer = forty_two;
//             ^ copy happens at assignment
fn take_ownership(of: u8) {}
take_ownership(the_answer);
//             ^ copy happens also when ownership required
println!("The answer is {}", the_answer);
//                           ^ can be reused since copied
```

[📒](https://doc.rust-lang.org/std/marker/trait.Copy.html)