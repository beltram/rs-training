## instantiate

* Value are namespaced with enum identifier (use of double colon) 
* different enums can contain same variant names

```rust
// Both values are of City type
let annecy = City::Annecy; 
let nantes = City::Nantes;

// data is attached to enum variant directly
let kleber = City::Paris(16);
let el_paso = City::Juarez(String::from("USA"));
```

[📒](https://doc.rust-lang.org/1.17.0/book/enums.html)