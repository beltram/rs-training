## impl

```rust
struct MyStruct { name: String, }
impl MyStruct {
    fn a_method(&self) {}
    fn a_mutable_method(&mut self) {}
    fn a_method_taking_ownership(self) {}
    fn a_static_method() {}
    // you can use 'Self' to reference current struct
    fn use_self_type(self) -> Self { Self { name: String::new() } }
}
fn main() {
    let mine = MyStruct { name: "".to_string() };
    mine.a_method();
    mine.a_method_taking_ownership(); // cannot use mine after this
    let mut mut_mine = MyStruct { name: "".to_string() };
    mut_mine.a_mutable_method();
    MyStruct::a_static_method();
}
```

[📒](https://doc.rust-lang.org/1.17.0/book/structs.html)