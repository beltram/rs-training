## polymorphism

* only Sized args are allowed
* hence trait must be boxed (dynamic dispatch)

```rust
fn destroy(vehicle: Box<dyn Vehicle>) {}

fn main() {
    let purchase = buy();
    println!("{}", purchase.serial());
    destroy(Box::new(purchase));
}
```