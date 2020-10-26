## advanced associated types

```rust
trait Map<'a> {
    type K: Hash; // single bound
    type V: Display + PartialEq; // many bound
    type A : 'a; // lifetime bound
    type T = String; // still unstable
}
```

* 'default associated type' can be activated through compiler option on nightly

[📒](https://doc.rust-lang.org/1.17.0/book/associated-types.html)