## Maybe sized

* a struct accepting a dynamically sized type

```rust
// read as 'T may or may not be Sized'
struct Unsized<T: ?Sized> {
    maybe_sized: T,
}
```

[📒](https://doc.rust-lang.org/1.17.0/book/unsized-types.html#sized)