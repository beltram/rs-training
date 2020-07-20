## impl Trait for Struct

```rust
struct Peach { weight: f64 }
trait Composable {
    fn sum(&self, other: Self) -> f64;
    //                   ^ Self represents the struct implementing this trait
}
//++++++++++++++++++++++++++++++++++
/**/ impl Composable for Peach { /**/
//++++++++++++++++++++++++++++++++++
    fn sum(&self, other: Self) -> f64 {
        self.weight + other.weight
    }
}
```

[📒](https://doc.rust-lang.org/1.17.0/book/traits.html)