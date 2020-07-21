## [Clone](https://doc.rust-lang.org/core/clone/trait.Clone.html)

* for explicit deep copy
* differs from [Copy](https://doc.rust-lang.org/std/marker/trait.Copy.html) by explicit nature. Indicates potential expensive deep copies.
* implement with derive macro. All fields must implement Clone
* any type can be Clone

```rust
#[derive(Clone)]
struct TheAnswer { value: String }

let forty_two = TheAnswer { value: String::from("42") };
let the_answer = forty_two.clone();
```

[📒](https://doc.rust-lang.org/core/clone/trait.Clone.html)