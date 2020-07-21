## [Ord](https://doc.rust-lang.org/std/cmp/trait.Ord.html), [PartialOrd](https://doc.rust-lang.org/std/cmp/trait.PartialOrd.html)

* [PartialOrd](https://doc.rust-lang.org/std/cmp/trait.PartialOrd.html) requires [PartialEq](https://doc.rust-lang.org/std/cmp/trait.PartialEq.html)
* [Ord](https://doc.rust-lang.org/std/cmp/trait.Ord.html) requires [Eq](https://doc.rust-lang.org/std/cmp/trait.Eq.html), [PartialEq](https://doc.rust-lang.org/std/cmp/trait.PartialEq.html) and [PartialOrd](https://doc.rust-lang.org/std/cmp/trait.PartialOrd.html)

```rust
#[derive(Eq, PartialEq, Ord, PartialOrd)]
struct Route { weight: u8 }

#[derive(Eq, PartialEq)]
struct BenjButton { age: u16 }
impl Ord for BenjButton {
    fn cmp(&self, other: &Self) -> Ordering {
        self.age.cmp(&other.age).reverse()
    }
}
impl PartialOrd for BenjButton {
    fn partial_cmp(&self, other: &Self) -> Option<Ordering> {
        self.age.partial_cmp(&other.age).map(|it| it.reverse())
    }
}
```