## Pattern matching

```rust
let year: u16 = 2018;
match year {
    1998 | 2018 => println!("France"),
    2014 => println!("Germany"),
    ref y if y%2 != 0 => println!("No world cup"),
    1958..=1962 => println!("Brazil"),
    _ => println!("No data")
}
```
[📒](https://doc.rust-lang.org/1.17.0/book/match.html) | 
[📒](https://doc.rust-lang.org/1.17.0/book/patterns.html) | 
[💻](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=dc55de878fcddacaa8dea2c226f52e44)
