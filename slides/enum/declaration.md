## declaration

* Different from enums in jvm languages
* looks a lot like [Kotlin sealed classes](https://kotlinlang.org/docs/reference/sealed-classes.html)
* An enum variant is a type in itself (pretty similar to struct declaration)
* UpperCamelCase name of variants

```rust
enum City {
    Nantes, // comma separated declaration (just like struct)
    Annecy,
    Juarez(String), // each variant can have associated data
    // (Juarez is the name of the city on Mexico side, El Paso on US side)
    Paris { district: u8 }, // data can be named explicitely
}
```

[📒](https://doc.rust-lang.org/1.17.0/book/enums.html)