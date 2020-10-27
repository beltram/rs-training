## range

* Ranges are only allowed with numeric values and char
* rustc ensures range is not empty at compile time

```rust
let x = 3;
match x {
    1..=3 => println!("one through three"), // equivalent to '1 | 2 | 3'
    _ => println!("something else"),
}

let x = 'c';
match x {
    'a'..='j' => println!("early ASCII letter"),
    'k'..='z' => println!("late ASCII letter"),
    _ => println!("something else"),
}
```

[📒](https://doc.rust-lang.org/book/ch18-03-pattern-syntax.html#matching-ranges-of-values-with-)