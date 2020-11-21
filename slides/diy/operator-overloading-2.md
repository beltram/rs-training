## Overload Addition

```rust
impl Add for Coord {
    type Output = Self;

    fn add(self, other: Self) -> Self {
        Self {
           x: self.x + other.x,
           y: self.y + other.y,
           z: self.z + other.z,
        }
    }
}
```

[⏯](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=3d8781f42383089f313eea0df1b536ee)