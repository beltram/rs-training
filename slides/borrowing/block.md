## A block

```rust
fn main() { // <- main block starts
    let a = "a";
    { // <- anonymous block starts
        let b = "b";
    } // <- anonymous block ends
    vec![1, 2, 3].into_iter().filter(|&it| it == 2);
    // a closure is a block ; start ^         end ^
    fn salute(who: String) { // <- salute block starts
        println!("Hello {}", who);
    } // <- salute block ends
} // <- main block ends
```