## if let

```rust
if let is_true = true { println!("this is {}", is_true); }
enum Store { Bakery, Supermarket(u32) }
let store = Store::Supermarket(75012);
// helps matching enums not implementing PartialEq
if let Store::Bakery = store { println!("bread !"); }
// also helps destructuring parameterized enum variants 
if let Store::Supermarket(departement) = store {
    println!("store is in departement {}", departement)
}
```

[📒](https://doc.rust-lang.org/stable/rust-by-example/flow_control/if_let.html)