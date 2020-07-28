## [Drop](https://doc.rust-lang.org/std/ops/trait.Drop.html)

* allows observing deallocation
* might be used to also drop remote resources e.g. a struct holding a reference to remote blob, a local temp file

```rust
struct Agent { name: String }
impl Drop for Agent {
    fn drop(&mut self) { println!("Dropping agent {}", self.name) }
}
fn main() {
    {
        let mib = Agent { name: String::from("K") };
    } // > Dropping agent K
    let bond = Agent { name: String::from("Bond") };
    let smith = Agent { name: String::from("Smith") };
}
// > Dropping agent Smith
// > Dropping agent Bond
```