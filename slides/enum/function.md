## function with enum

```rust
// use an enum as function arg
fn population(city: City) -> u32 { unimplemented!() }

// call the function with a variant
population(City::Nantes);
```

[📒](https://doc.rust-lang.org/1.17.0/book/enums.html)
