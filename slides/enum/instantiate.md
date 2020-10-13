## instantiate

* enum values are namespaced with enum identifier and double colon :: 
* different enums can contain same variant names, of course

```rust
// both values are of City type
let annecy: City = City::Annecy; 
let nantes = City::Nantes;

// attribute is attached to enum variant directly
let kleber = City::Paris(16);
let el_paso = City::Juarez(String::from("USA"));
```

[📒](https://doc.rust-lang.org/1.17.0/book/enums.html)