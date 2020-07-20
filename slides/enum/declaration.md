## declaration

* An enum is a type in itself (pretty similar to struct declaration)
* one block for fields declaration
* UpperCamelCase name

```rust
enum Workplace { // all valid possibilities SHOULD be listed
    Paris, // comma separated declaration (just like struct)
    Nantes,
	Annecy,
	Bruxelles,
}

enum WorkplaceDetailed {
	Paris(String), // enum's variants can have data
	Nantes(String),
}
```

[📒](https://doc.rust-lang.org/1.17.0/book/enums.html)