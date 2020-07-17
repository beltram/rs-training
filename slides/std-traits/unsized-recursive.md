## Infinite size

```rust
// recursive struct
struct Fibonacci {
// ERROR ^^^^^^ recursive type has infinite size
    current: u32,
    next: Self,
}
struct Fibonacci {
    current: u32,
    next: Box<Self>,
}
```