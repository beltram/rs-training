## while let

* while let is similar to if let but allow a conditional loop as long as the pattern match

```rust
let mut stack = Vec::new();

stack.push(1);
stack.push(2);
stack.push(3);

// pop() method takes last element of a vector and return Some(value)
// or None if vector is empty
while let Some(top) = stack.pop() {
    println!("{}", top);
}
```

[📒](https://doc.rust-lang.org/book/ch18-01-all-the-places-for-patterns.html#while-let-conditional-loops)