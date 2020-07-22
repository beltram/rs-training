## @ binding operator

* Allows to test a value from a variable and bind it directly to an inner variable

```rust
enum Message {
    Answer { id: i32 },
}

let msg = Message::Answer { id: 42 };

match msg {
    Message::Answer { id: id_variable @ 3..=7, // var tested and code knows it
    } => println!("Found an answer in range: {}", id_variable),
    Message::Answer { id: 42 } => { // var tested but code don't know it
        println!("Greatest answer ever")
    }
    // var not tested but code knows it
    Message::Answer { id } => println!("Found some other answer: {}", id),
}
```

[📒](https://doc.rust-lang.org/book/ch18-03-pattern-syntax.html#-bindings)