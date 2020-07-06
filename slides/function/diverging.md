## diverging functions

* functions that do not return
* use ! type
* can be assigned to any type
* similar to 'Nothing' type in Kotlin

```rust
fn diverging() -> ! {
    panic!("'diverging' never returns");
}
fn main() {
    // can be assigned to any type
    let a_string: String = diverging();
    // you cannot explicitly declare ': !', just for demonstration here
    let defaults_to_exclamation_mark: ! = diverging(); // this does not compile
}
```

[📒](https://doc.rust-lang.org/1.17.0/book/functions.html#diverging-functions)