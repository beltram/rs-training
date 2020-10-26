## default generics

* sometimes, you know that most of the time a generic will be of a certain type

```rust
trait Multiple<R> {
    fn ppcm(self, other: R) -> Self;
}

impl Multiple<u32> for u32 {
//           ^^^^^ boring 😕
    fn ppcm(self, other: Self) -> Self { unimplemented!() }
}
```

[📒](https://doc.rust-lang.org/book/ch19-03-advanced-traits.html#default-generic-type-parameters-and-operator-overloading)