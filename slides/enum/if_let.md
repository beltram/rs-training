## if let control flow with enum

* syntactic sugar when you only require partial matching

```rust
let home = City::Nantes;
if let City::Paris { district } = home {
    println!("I live in Paris {}th district", district);
} else if let City::Juarez(country) = home {
    println!("I'm an {} citizen living in Juarez", country);
}
// equivalent to
let home = City::Nantes;
match home {
    City::Paris { district } => println!("..in Paris {}th district", district),
    City::Juarez(country) => println!("I'm an {} .. Juarez", country),
    _ => {}
}
```

[📒](https://doc.rust-lang.org/book/ch06-03-if-let.html)