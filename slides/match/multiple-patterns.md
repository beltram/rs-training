## multiple patterns

```rust
let x = 1;

match x {
    1 | 2 => println!("one or two"), // the | operator means or
    3 => println!("three"),
    _ => println!("anything"),
}
```

[📒](https://doc.rust-lang.org/book/ch18-03-pattern-syntax.html#multiple-patterns)