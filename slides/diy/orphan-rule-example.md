## orphan rule

* If you really need to, you can still (re)implement external traits on external types

```rust
use std::fmt;
// Wrappe the type into a tuple struct you own
// This is zero cost abstraction - no runtime cost
struct MyType(String);

impl fmt::Display for MyType {
    fn fmt(&self, f: &mut fmt::Formatter<'_>) -> fmt::Result {
        write!(f, "{}!!", self.0)
    }
}
fn main() {

    let my_var = MyType(String::from("Test"));
    println!("{}", my_var); // print Test!!
}
```