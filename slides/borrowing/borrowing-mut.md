## mutable borrow

* '&mut' for a mutable borrow
* a variable has to be mutable to borrow it with mutability

```rust
// Very ugly ! Do not ever write something like this
fn capitalize(of: &mut String) {
    of.clone().chars().enumerate().for_each(|(index, it)| {
        of.remove(index);
        of.insert(index, it.to_ascii_uppercase());
    });
}
let mut beltram = String::from("beltram");
capitalize(&mut beltram);
assert_eq!("BELTRAM", beltram);
```