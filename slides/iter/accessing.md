## get elements

* Vec are zero indexed

```rust
let v = vec!["a", "e", "i"];
assert_eq!("a", v[0]);
assert_eq!("i", v[2]);
// Safe access
v.get(1).map(|e| println!("Safe access to {}", e));
if let Some(a) = v.get(0) {
    println!("Safe access to {}", a)
}
// Out-of-bounds access panics
assert_eq!(false, v.get(3).is_some());
```

[📒](https://doc.rust-lang.org/1.17.0/book/vectors.html#accessing-elements) 