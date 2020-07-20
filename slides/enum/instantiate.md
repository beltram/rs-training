## instantiate

* Value are namespaced with enum identifier (use of double colon) 
* different enum can contains same variant names
```rust
fn main() {
    // Both values are of Workplace type
    let paris = Workplace::Paris; 
    let nantes = Workplace::Nantes;

    // data is attached to enum variant directly
    let kleber = WorkplaceDetailed::Paris(String::from("Kleber")); 
}
```

[📒](https://doc.rust-lang.org/1.17.0/book/enums.html)