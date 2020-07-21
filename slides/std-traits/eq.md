## [Eq](https://doc.rust-lang.org/std/cmp/trait.Eq.html), [PartialEq](https://doc.rust-lang.org/std/cmp/trait.PartialEq.html)

|  Property | Example | PartialEq | Eq |
|:-------:|:------:|:-------:|:-------:|
|reflexive|a == a|🔴|🟢|
|symetric|a == b implies b == a|🟢|🟢|
|transitive|a == b and b == c implies a == c|🟢|🟢|

```rust
assert_ne!(f32::NAN, f32::NAN); // so f32 impl PartialEq but does NOT impl Eq
// also PartialEq is Eq supertrait
pub trait Eq: PartialEq {}
```