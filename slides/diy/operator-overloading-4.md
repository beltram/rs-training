## Permutation of the operands

```rust
impl Mul<i32> for Coord {
    type Output = Self;

    fn mul(self, coef: i32) -> Self {
        Self::new(coef * self.x, y: coef * self.y, z: coef * self.z)
    }
}

impl Mul<Coord> for i32 {
    type Output = Coord;

    fn mul(self, coord: Coord) -> Coord {
        coord * self
    }
}
```

[⏯](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=7e0c61e0047f46673f68afc6b4e59b20)