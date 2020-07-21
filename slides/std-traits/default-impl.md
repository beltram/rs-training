## impl [Default](https://doc.rust-lang.org/std/default/trait.Default.html) explicitly

* when a field does not implement Default

```rust
struct Galaxy { name: String }
struct Planet {
    habitable: bool,
    belongs_to: Galaxy,
    //          ^ does not impl Default so we cannot use derive macro
}

impl Default for Planet {
    fn default() -> Self {
        Self {
            habitable: bool::default(),
            belongs_to: Galaxy { name: String::default() },
        }
    }
}
```