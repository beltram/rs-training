## basics

```rust
let x = 1;

match x {
    1 => println!("one"),
    _ => println!("anything"), // used as default or else
}

match x {
    // match any value and create a binding y for the value
    y => println!("x: {} y: {}", x, y), 
    _ => println!("anything"), // this causes an error as it is unreachable
}
```

[📒](https://doc.rust-lang.org/1.17.0/book/patterns.html)