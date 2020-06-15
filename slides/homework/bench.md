## Cargo bench

```rust
#![feature(test)]
extern crate test;
pub fn add_two(a: i32) -> i32 { a + 2 }
#[cfg(test)]
mod tests {
    use super::*;
    use test::Bencher;

    #[bench]
    fn bench_add_two(b: &mut Bencher) {
        b.iter(|| add_two(2));
    }
}
```

[📒](https://doc.rust-lang.org/cargo/commands/cargo-bench.html) | 
[💻](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=47c0726f5caf02a8260e9bbc62f3f168)