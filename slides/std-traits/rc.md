## Rc

```rust
use std::rc::Rc;
struct Person { firstname: Rc<String> }

let name = Rc::new(String::from("beltram"));
assert_eq!(1, Rc::strong_count(&name));
let a = Person { firstname: Rc::clone(&name) };
assert_eq!(2, Rc::strong_count(&name));
//         ^ cloning the Rc has increased its counter
{
    let b = Person { firstname: name.clone() };
    //                          ------------ equivalent to Rc::clone()
    assert_eq!(3, Rc::strong_count(&name));
} // <- b is dropped here so is its 'firstname' field
assert_eq!(2, Rc::strong_count(&name));
//         ^ hence the RC counter is decremented
```