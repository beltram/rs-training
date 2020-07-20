## [E0038](https://doc.rust-lang.org/error-index.html#E0038): no const allowed

* NO const declaration allowed

```rust
trait Formula {
    // ------ this trait cannot be made into an object...
    const importance: u8;
    //    ---------- ...because it contains this associated `const`
    fn is_installed(&self) -> bool;
}
```

[📒](https://doc.rust-lang.org/error-index.html#the-trait-cannot-contain-associated-constants)