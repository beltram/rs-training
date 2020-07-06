## default

```rust
// Default derive macro will use each field 'default()'
#[derive(Default)]
struct Person {
    name: String,
    age: u8,
}
// explicit default by trait
impl Default for Person {
    fn default() -> Self {
        Self {
            name: "unknown".to_string(),
            age: 0,
        }
    }
}
```

[📒](https://doc.rust-lang.org/1.7.0/book/structs.html)