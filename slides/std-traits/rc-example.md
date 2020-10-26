## [Rc](https://doc.rust-lang.org/std/rc/struct.Rc.html)

* stands for 'reference counter'
* when multiple ownership is required
* see also [Arc](https://doc.rust-lang.org/std/sync/struct.Arc.html) for atomic variant
---
Given this example which does not compile. We want to fix it without performing deep copy.

```rust
struct Person { firstname: String }
let name = String::from("beltram");

let a = Person { firstname: name };
//                          ---- value moved here
let b = Person { firstname: name };
//                          ^^^^ value used here after move
```

[📒](https://doc.rust-lang.org/rust-by-example/std/rc.html)