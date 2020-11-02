## function

* there is an extra possibility when documenting a function. You can write specific text for args
* you cannot document return type though

```rust
/// Brief.
///
/// Description.
/// 
/// * `foo` - Text about foo.
/// * `bar` - Text about bar.
fn a_function(foo: i32, bar: &str) {}
```