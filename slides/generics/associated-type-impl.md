## associated types implementation

* each associated must be defined when trait implemented

```rust
struct Doy {}
struct Calendar {}

impl Map for Calendar {
    type K = Doy;
    type V = String;

    fn add(&self, key: Self::K, value: Self::V) -> bool { unimplemented!() }
}
```

* or declare them <a href="#/10/17">like this</a> on polymorphic return types

[📒](https://doc.rust-lang.org/1.17.0/book/associated-types.html#implementing-associated-types)