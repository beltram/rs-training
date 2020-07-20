## [E0038](https://doc.rust-lang.org/error-index.html#E0038): no generic allowed

* NO type parameter declared on a method allowed

```rust
trait Formula {
    // ------ this trait cannot be made into an object...
    fn requires<T>(&self, required: T);
    // -------- ...because method `requires` has generic type parameters
}
```

[📒](https://doc.rust-lang.org/error-index.html#method-has-generic-type-parameters)