## e.g. returning an iterator

```rust
fn even<'a>(suite: &'a Vec<u32>) -> impl Iterator<Item=&'a u32> {
    suite.iter().filter(|&it| it % 2 == 0)
}
```

[📒](https://doc.rust-lang.org/rust-by-example/trait/impl_trait.html)