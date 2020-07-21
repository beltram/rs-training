## polymorphism

* use 'impl my-trait' syntax to declare that return type behaves as a trait
* cannot be used for args or variables type declaration

```rust
trait Vehicle {
    fn serial(&self) -> &'static str { "1234" }
}
struct Car {}
struct Moto {}
impl Vehicle for Car {}
impl Vehicle for Moto {}

fn buy() -> impl Vehicle { Car {} }
fn main() {
    let purchase = buy();
    println!("{}", purchase.serial());
}
```

[📒](https://doc.rust-lang.org/rust-by-example/trait/impl_trait.html)