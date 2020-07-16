## iter with for

```rust
let mut vec = vec![1, 2, 3, 4, 5];
for i /*:&i32*/  in &vec {
    println!("A reference to {}", i);
}
for i/*:&mut i32*/ in &mut vec {
    println!("A mutable reference to {}", i);
}
for i/*:i32*/ in vec {
    println!("Take ownership of the vec and its element {}", i);
}
```

[📒](https://doc.rust-lang.org/1.17.0/book/vectors.html#iterating) 