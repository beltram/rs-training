## instantiate

```rust
struct Person { 
    name: String, 
    age: u8,
}
fn main() {
    let instance = Person { name: "beltram".to_string(), age: 29, };
    let name = "beltram".to_string();
    // you can init a 'name' field by a 'name' local variable
    let instance = Person { name, age: 29, };
    let name = instance.name; // access fields with dot notation
    // create a new instance from an other. Called 'update syntax'
    let copy_from_other_instance = Person { age: 30, ..instance };
}
```

[📒](https://doc.rust-lang.org/1.17.0/book/structs.html)