## [Default](https://doc.rust-lang.org/std/default/trait.Default.html)

* allows defining default values of a struct fields

---
* prefer derive macro if possible
* all fields types have to implement default

```rust
#[derive(Default)]
struct Planet {
    age: u32,
    name: String,
    habitable: bool,
}
// will use u32, String and bool defaults
```