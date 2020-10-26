## @ binding operator

* allows testing a value from a variable and bind it directly to an inner variable

```rust
enum Message { Answer { id: i32 } }
let msg = Message::Answer { id: 5 };

match msg {
    Message::Answer { id: id_var @ 0..10, } => println!("figure: {}", id_var),
    // 'id_var' is in [0,10[     ^^^^^^^
    Message::Answer { id: 10..=20 } => println!("from 10 to 20"),
    // 'id' is in [10,20] but we cannot use it in println
    Message::Answer { id: 42 } => println!("Greatest answer ever"),
    // 'id' is 42 but we cannot use it in println
    Message::Answer { id } => println!("Found some other answer: {}", id),
}
```

[📒](https://doc.rust-lang.org/book/ch18-03-pattern-syntax.html#-bindings)