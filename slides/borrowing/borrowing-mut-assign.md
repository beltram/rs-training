## mutable borrow assignment

* mutable reference should be dereferenced to be mutated 
* prefix variable with * to dereference

```rust
fn emojize(letter: &mut String) {
    *letter = String::from("🦀");
}
let mut a = String::from("A");
emojize(&mut a);
assert_eq!(String::from("🦀"), a);
```