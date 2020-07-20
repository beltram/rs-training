## enum impl

```rust
// any variant with the same function signature 
// instead of of having 4 different types
impl City {
    fn get_mayor(&self) -> &'static str {
        match self {
            City::Paris { district } => match district {
                0 => "Anne Hidalgo",
                _ => "",
            },
            _ => "",
        }
    }
}
// we can enforce specific behavior directly from enum variant and its data
let anne_hidalgo = City::Paris(0).get_mayor();
```

[📒](https://doc.rust-lang.org/1.17.0/book/enums.html)
