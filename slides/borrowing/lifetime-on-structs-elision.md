## lifetime on structs elision

```rust
struct Person<'a> { firstname: &'a str }

impl<'a> Person<'a> {
    // explicit lifetime declaration required
    fn lifetime_in_signature(&self) -> &'a str { self.firstname }
    // because lifetime part of ABI    ^^^
}

impl Person<'_> {
//           ^ elided lifetime
    fn lifetime_less(&self) -> String { self.firstname.to_string() }
    // because not part of ABI ^^^^^^
}
```