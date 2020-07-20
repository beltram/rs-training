## closure move

* use 'move' to explicitly take ownership
* very common while spawning threads (they outlive main thread so they require ownership)

```rust
let greeting = String::from("Hello ");
// here 'welcome' takes ownership of 'greeting'
let welcome = move |it: &str| println!("{}{}", greeting, it);
// println!("{}", greeting);
// ERROR          ^^^^^^^^ value borrowed here after move
```

[📒](https://doc.rust-lang.org/1.17.0/book/closures.html#move-closures)