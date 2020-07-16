## for

```rust
for i in 0..10 {
    println!("i -> {}", i);
}
// 0 to 10
for i in 0..=10 { println!("i -> {}", i); }
let vowels = vec!["a", "e", "i", "o", "u", "y"];
// because Vec implements IntoIterator trait
for v in vowels {
    println!("v -> {}", v);
}
```

[📒](https://doc.rust-lang.org/1.17.0/book/loops.html#for)