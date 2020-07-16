## Vec in memory

* contiguous memory layout

```rust
// pseudo-code
struct Vec<T> {
    ptr: *mut T,
    len: usize,
    cap: usize,
}
```

```rust
let vec = vec![0; 10];
assert_eq!(24, std::mem::size_of_val(&vec));
let vec = vec![0; 10_000];
assert_eq!(24, std::mem::size_of_val(&vec));
```

[📒](https://doc.rust-lang.org/1.17.0/book/vectors.html#vectors)