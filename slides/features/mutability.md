## Immutable by default 

```rust
struct Politician { pub party: String }
fn prepare_elections() -> Politician {
    let mut politician = Politician {
        party: "some".to_string()
    };
    politician.party = "other".to_string();
    politician
}
```

[📒](https://doc.rust-lang.org/1.7.0/book/mutability.html) | 
[💻](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=3ef3adb0095e04b18cccdac468cad40b)