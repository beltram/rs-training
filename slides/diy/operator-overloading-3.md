## Overload operator and self assign

```rust
impl AddAssign for Coord {
    fn add_assign(&mut self, other: Coord) {
        *self = *self + other;
    }
}
```

Important: `self` is passed as mutable reference

[⏯](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=cae17a3fdb51e0eddf89ff0e92410473)