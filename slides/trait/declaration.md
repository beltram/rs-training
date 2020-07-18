## trait

* using 'trait' keyword

```rust
trait Interface {
    fn hash(&self) -> u8; // borrowed implementer
    fn destroy(self); // owned implementer
    fn change_id(&mut self); // borrowed implementer
    fn as_str() -> String; // static method
}
```

[📒](https://doc.rust-lang.org/1.17.0/book/traits.html)