## function

* There is an extra possibility when documenting a function. You can write specific text for args (not return type though)

```rust
/// Brief.
///
/// Description.
/// 
/// * `foo` - Text about foo.
/// * `bar` - Text about bar.
fn function (foo: i32, bar: &str) {}
```