## Allocation

```rust
fn main() {
    // variable bindings have 'move semantics' ie 'v' takes ownership of vec![]
    let v: Vec<i32> = vec![1, 2, 3, 4, 5];
    // allocates 24 bytes on stack frame and 5x4 bytes on the heap
} // <- end of block owning v
// 24 bytes on stack frame and 5x4 bytes on the heap are freed
```

[📒](https://doc.rust-lang.org/1.17.0/book/ownership.html#ownership)