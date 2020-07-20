## declaration

* Different from enums in jvm languages
* An enum is a type in itself (pretty similar to struct declaration)
* UpperCamelCase name of variants

```rust
enum City {
    Nantes, // comma separated declaration (just like struct)
    Annecy,
    Juarez(String), // each variant can have associated data
    Paris { district: u8 }, // data can be named explicitely
}
```

[📒](https://doc.rust-lang.org/1.17.0/book/enums.html)