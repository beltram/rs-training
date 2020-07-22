## Move semantics: struct field

```rust
struct Landlord { house: String }
fn main() {
    let buckingham = String::from("Buckingham");
    //  ---------- move occurs because `buckingham` does not implement `Copy`
    let elizabeth = Landlord { house: buckingham };
    //                                ---------- value moved here
    let british_crown = Landlord { house: buckingham };
    //                                    ^^^^^^^^^^ value used here after move
}
```

[📒](https://doc.rust-lang.org/1.17.0/book/ownership.html#move-semantics)