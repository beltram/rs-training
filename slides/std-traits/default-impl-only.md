## impl [Default](https://doc.rust-lang.org/std/default/trait.Default.html) only non-default fields

* would be sad if we had to declare default for each field when ONLY 1 is not default

```rust
struct Galaxy { name: String }
struct Planet { age: u32, habitable: bool, belongs_to: Galaxy }
impl Default for Planet {
    fn default() -> Self {
        Self {
            belongs_to: Galaxy { name: String::default() },
            ..Default::default() // <- fills 'age' & 'habitable' defaults
        }
    }
}
```