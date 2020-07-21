## declare my struct [Copy](https://doc.rust-lang.org/std/marker/trait.Copy.html)

* always use derive macro
* [Copy](https://doc.rust-lang.org/std/marker/trait.Copy.html) requires [Clone](https://doc.rust-lang.org/core/clone/trait.Clone.html)

```rust
#[derive(Copy, Clone)]
struct Answer {}

// NOT recommended
struct TheAnswer {}
impl Copy for TheAnswer {}
impl Clone for TheAnswer {
    fn clone(&self) -> Self { *self }
}
```

[📒](https://doc.rust-lang.org/std/marker/trait.Copy.html#how-can-i-implement-copy)