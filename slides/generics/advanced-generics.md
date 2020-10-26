## advanced generics

* a generic bound can be valid only for a given lifetime
* called 'Higher-ranked trait bounds'

```rust
pub trait Jsonable where for<'de> Self: Deserialize<'de> + Debug {
    fn from_json(content: String) -> Self {
        serde_json::from_str(&content).expect("ooops")
    }
}
```

[📒](https://doc.rust-lang.org/reference/trait-bounds.html#higher-ranked-trait-bounds)