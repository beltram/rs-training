## if let

* if let can be used as a shorter syntax for match but it can be used in combination with else/else if/else if let

```rust
let favorite_color: Option<&str> = None;
let is_tuesday = false;
let age: Result<u8, _> = "34".parse();

if let Some(color) = favorite_color {
    println!("Using your favorite color, {}, as the background", color);
} else if is_tuesday {
    println!("Tuesday is green day!");
} else if let Ok(age) = age {
    if age > 30 {
        println!("Using purple as the background color");
    }
} else {
    println!("Using blue as the background color");
}
```

[📒](https://doc.rust-lang.org/book/ch18-01-all-the-places-for-patterns.html#conditional-if-let-expressions)
[💻](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=557976e1b544c5e34e59eb09dc7348f6)