## many mutable borrow

* a variable can only be mutably borrowed ONCE
* a variable cannot be both mutably & immutably borrowed

```rust
fn many_borrow(a: &String, b: &String) {}
fn many_mut_borrow(a: &mut String, b: &mut String) {}
fn maybe_many_mut_borrow(a: &mut String, b: &String) {}
let (mut a, mut b) = (String::from("a"), String::from("b"));
many_borrow(&a, &a); // OK, immutable borrow
many_mut_borrow(&mut a, &mut b); // OK, 'a' memory location != 'b'
many_mut_borrow(&mut a, &mut a); // ERROR, 'a' borrowed mutably twice
maybe_many_mut_borrow(&mut a, &a); // ERROR, 'a' is borrowed mutably & immutably
```