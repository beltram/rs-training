## [E0038](https://doc.rust-lang.org/error-index.html#E0038): no static method allowed

* NO static trait method (no &self) is allowed

```rust
trait Formula {
//    ------- this trait cannot be made into an object...
    fn is_installed(&self) -> bool;
    fn name() -> &'static str;
//     ---- ...because associated function `name` has no `self` parameter
}

// help: consider turning `name` into a method by giving it a `&self` argument or constraining it so it does not apply to trait objects
// 2 possible fixes
// fn name() -> &'static str where Self: Sized;
// fn name(&self) -> &'static str;
```

[📒](https://doc.rust-lang.org/error-index.html#method-has-no-receiver)