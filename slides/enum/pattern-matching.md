## enum pattern matching

* match expression on enums MUST be exhaustive
* use _ as 'default' (Java) or 'else' (Kotlin)

```Rust
fn get_city_insight(city: City) {
    match city {
        City::Nantes => println!("Beltram's home..."),
        City::Paris { district } => println!("Paris' {}th", district),
        //            ^^^^^^^^ named variant data between { }
        City::Juarez(country) => println!("Juarez in {}", country),
        //           ^^^^^^^ anonymous variant data between ( )
        _ => println!("Has to be Annecy then.."),
    }
}
```

[📒](https://doc.rust-lang.org/book/ch06-02-match.html)