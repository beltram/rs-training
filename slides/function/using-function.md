## using a function

```rust
fn hello() { println!("hello"); }
fn salute(name: &str) { println!("hello {}", name); }
fn initial(name: &str) -> &str { &name[..1] }

fn main() {
    hello();
    salute("beltram");
    let initial = initial("beltram");
    println!("hello Mr.{}", initial);
}
```

[📒](https://doc.rust-lang.org/1.7.0/book/functions.html)