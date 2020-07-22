## Borrowing

* prefix type with &
* variable not deallocated after borrow ends

```rust
fn salute(of: &String) { println!("Hello {}", of); }
let beltram = String::from("Beltram");
salute(&beltram);
println!("{} hasn't been moved", beltram);
```