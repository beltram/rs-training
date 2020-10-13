## if let control flow with enum

* syntactic sugar when you only require partial matching
* also helps when enum does not implement [PartialEq](https://doc.rust-lang.org/std/cmp/trait.PartialEq.html)

```rust
let home = City::Nantes;
if let City::Paris { district } = home {
    println!("I live in Paris {}th district", district);
} else if let City::Juarez(country) = home {
    println!("I'm an {} citizen living in Juarez", country);
}
// equivalent to
match home {
    City::Paris { district } => println!("..in Paris {}th district", district),
    City::Juarez(country) => println!("I'm an {} .. Juarez", country),
    _ => {}
}
```

[📒](https://doc.rust-lang.org/book/ch06-03-if-let.html)