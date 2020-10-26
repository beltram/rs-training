## associated types

* declare associated types using 'type' keyword
* at the beginning of struct/trait
* generics are now namespaced

```rust
trait Map {
    type K;
    type V;
    fn add(&self, key: Self::K, value: Self::V) -> bool;
    // namespaced      ^^^^^^^         ^^^^^^^
}

fn print_each<M: Map>(of: &M) {}
//            ^^^^^^ cleaner
fn read<M: Map>(of: &M, key: M::K) -> M::V { unimplemented!() }
//      namespaced under 'M' ^^^^     ^^^^
```

[📒](https://doc.rust-lang.org/1.17.0/book/associated-types.html)