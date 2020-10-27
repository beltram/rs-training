## destructuring enums

* enums can also be destructured using the way data is stored within the enum
* see a more complex example with nested struc and enums [here](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=71867092024da2b64b1fbc6a8b2101a4)

```rust
enum Message {
    Quit,
    Move { x: i32, y: i32 },
    ChangeColor(i32, i32, i32),
}
let msg = Message::ChangeColor(0, 160, 255);
match msg {
    Message::Quit => println!("No data to destructure."),
    Message::Move { x, y } => println!("Move x of {} and y of {}", x, y),
    Message::ChangeColor(r, g, b) => println!("R:{}, G:{}, B:{}", r, g, b),
}
```

[📒](https://doc.rust-lang.org/book/ch18-03-pattern-syntax.html#destructuring-enums)