## associated types

* sometimes, generics are only meaningful when used with others
* sometimes, generics are only meaningful in a certain context

```rust
trait Map<K, V> {
    fn add(&self, key: K, value: V) -> bool;
}

fn print_each<K, V, M: Map<K, V>>(of: &M) {}
//            ^^^^^^^^^^^^^^^^^ boring 😕
fn read<K, V, M: Map<K, V>>(of: &M, key: K) -> V { unimplemented!() }
```

* I don't want every function generic over 'Map' to also be generic over 'K' and 'V'
* 'K' and 'V' are never to be used without 'Map'

[📒](https://doc.rust-lang.org/1.17.0/book/associated-types.html)