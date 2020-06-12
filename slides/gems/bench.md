## Cargo bench
<img src="lib/images/cargo-bench.svg" style="height:40vh"/>  
[📒](https://doc.rust-lang.org/cargo/commands/cargo-bench.html) | 
[💻](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=47c0726f5caf02a8260e9bbc62f3f168)

<!--
#![feature(test)]

extern crate test;

pub fn add_two(a: i32) -> i32 {
    a + 2
}

#[cfg(test)]
mod tests {
    use super::*;
    use test::Bencher;

    #[test]
    fn it_works() {
        assert_eq!(4, add_two(2));
    }

    #[bench]
    fn bench_add_two(b: &mut Bencher) {
        b.iter(|| add_two(2));
    }
}
-->