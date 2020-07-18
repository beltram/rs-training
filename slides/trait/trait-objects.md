## Trait Objects

* see [E0038](https://doc.rust-lang.org/error-index.html#E0038)
* dynamic dispatch requires none of the trait methods to be static (no &self)

```rust
trait Formula {
//    ------- this trait cannot be made into an object...
    fn is_installed(&self) -> bool;
    fn name() -> &'static str;
//     ---- ...because associated function `name` has no `self` parameter
}
fn random_formula() -> Box<dyn Formula> {
//                     ^^^^^^^^^^^^^^^^ the trait `Formula` cannot be made into an object
    unimplemented!()
}
// help: consider turning `name` into a method by giving it a `&self` argument or constraining it so it does not apply to trait objects
// 2 possible fixes
// fn name() -> &'static str where Self: Sized;
// fn name(&self) -> &'static str;
```

[📒](https://doc.rust-lang.org/1.17.0/book/traits.html)