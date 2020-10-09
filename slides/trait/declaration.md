## trait

* using 'trait' keyword
* traits cannot have fields
* traits can have const

```rust
trait AkaInterface {
    fn hash(&self) -> u8; // borrowed implementer
    fn destroy(self); // owned implementer
    fn change_id(&mut self); // mutable borrowed implementer
    fn as_str() -> String; // static method
    const answer: u8 = 42;
    const variant_answer: u8;
}
```

[📒](https://doc.rust-lang.org/1.17.0/book/traits.html)