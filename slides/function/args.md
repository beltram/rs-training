## args

* no default value
* no vararg

```rust
fn no_arg() { } // () required
fn one_arg(name: &str) { }
fn two_arg(name: &str, age: u8) { }
// passing mutable arg
struct Person { name: String }
// here 'mut' is not part on method's signature ; it is a shorthand for turning the arg mutable
// for the function scope only since the function has ownership over the arg
fn one_mut_arg(mut person: Person) { person.name = "other".to_string(); }
fn one_mut_borrow_arg(person: &mut Person) { person.name = "other".to_string(); }
```

[📒](https://doc.rust-lang.org/1.17.0/book/functions.html)