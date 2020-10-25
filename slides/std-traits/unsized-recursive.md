## Infinite size

```rust
// recursive struct
struct Fibonacci {
// ERROR ^^^^^^ recursive type has infinite size
    current: u32,
    next: Self, // infinite size
}
// this compiles
struct Fibonacci {
    current: u32,
    next: Box<Self>, // a pointer is sized
}
```

[📒](https://doc.rust-lang.org/book/ch15-01-box.html#enabling-recursive-types-with-boxes)