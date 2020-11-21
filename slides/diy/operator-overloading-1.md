## Operator Overloading

Overload operators consists in implementing traits from `core::ops`

```rust
#[derive(Debug, Clone, Copy)]
struct Coord {
    x: i32,
    y: i32,
    z: i32,
}

impl Coord {
    fn new(x: i32, y: i32, z: i32) -> Self {
        Self { x: x, y: y, z: z }
    }
}
```

Important: We implement Clone and Copy traits to simplify the examples. You can have both T and &T implement the traits so that generic code can be written without unnecessary cloning.

Complete example [⏯](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=c5ea8995af3bc282d684aa2469db94e7)
[📒](https://doc.rust-lang.org/core/ops/)