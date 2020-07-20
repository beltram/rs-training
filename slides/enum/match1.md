## match control flow with enum

* match expression will be checked at compile time to make sure all possible cases are handled. If not you'll get a compile error

```Rust
fn get_city_insight(city: Workplace) -> () { 
    match city { // No need to handle None or generic cases as enum are exhaustives
        Workplace::Paris => println!("The place to be!"),
        Workplace::Nantes => println!("Beltram's home..."),
        Workplace::Annecy => println!("A city in France"),
        Workplace::Bruxelles => println!("A city not in France"),
    }
}

fn main() {
    get_city_insight(Workplace::Paris); // will print: The place to be! 
}
```

[📒](https://doc.rust-lang.org/book/ch06-02-match.html)