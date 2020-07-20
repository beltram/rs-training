## [E0038](https://doc.rust-lang.org/error-index.html#E0038): no reference to Self allowed

* NO reference to 'Self' in args or return type allowed

```rust
trait Formula {
    // ------ this trait cannot be made into an object...
    fn build(&self) -> Self;
    //                 ---- ...because method `build` references the `Self` type in its return type
    fn depends_on(&self, other: Self);
    //                   ---- ...because method `depends_on` references the `Self` type in this parameter
}
```

[📒](https://doc.rust-lang.org/error-index.html#method-references-the-self-type-in-its-parameters-or-return-type)