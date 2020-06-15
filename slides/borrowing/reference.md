## Borrowing 
###### Use reference or return

```rust
fn do_stuff() {
    let s1: String = String::from("hello");
    use_reference(&s1);
    let s1 = use_return(s1);
    use_return(s1);
}
/// 'hi' is borrowed here
fn use_reference(hi: &String) { println!("{:?} world", hi) }

/// 'to' is owned here
fn use_return(to: String) -> String {
    println!("{} -> 👋", to);
    to
}
```

[📒](https://doc.rust-lang.org/1.7.0/book/references-and-borrowing.html) | 
[💻](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=ea35bb5d7a990008c6badcb8a9cf719b)