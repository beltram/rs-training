## Move semantics: fn argument

```rust
fn welcome(who: String) { println!("Welcome {}", who); }
// 'welcome' takes ownership of 'who'
let hello = |who: String| println!("Hello {}", who); // same goes for closure
let beltram = String::from("Beltram");
//  ------- move occurs because `beltram` does not implement the `Copy` trait
welcome(beltram);
//      ------- value moved here
welcome(beltram);
//      ^^^^^^^ value used here after move
```

[📒](https://doc.rust-lang.org/1.17.0/book/ownership.html#move-semantics)