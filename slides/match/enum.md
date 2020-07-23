### destructuring enums

* Enums can also be destructured using the way the data is stored within the enum
* See a more complex example with nested struc and enums [here](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=71867092024da2b64b1fbc6a8b2101a4)

```rust
enum Message {
  Quit,
  Move { x: i32, y: i32 },
  ChangeColor(i32, i32, i32),
}
fn main() {
  let msg = Message::ChangeColor(0, 160, 255);
  match msg {
   Message::Quit => println!("No data to destructure."),
   Message::Move { x, y } => println!("Move x of {} and y of {}", x, y),
   Message::ChangeColor(r, g, b) => println!("red {},green {},blue {}", r, g, b),
  }
}
```

[📒](https://doc.rust-lang.org/book/ch18-03-pattern-syntax.html#destructuring-enums)