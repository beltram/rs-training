## declaration

* similar to jvm classes
* one block for fields declaration, one for methods
* UpperCamelCase name
* no default value for fields
* no mutability in struct declaration

```rust
struct NoFields;
pub struct PubStruct {} // a struct is by default private
struct WithFields {
    snake_case_fields: String, // comma separated declaration
    private_by_default: bool, // fields are by default private
    pub public_field: bool,
}
```

[📒](https://doc.rust-lang.org/1.7.0/book/structs.html)