## 'static lifetime

* lifetime valid for the entire program
* already seen on string literals
* implicit on string literals
* baked into the data segment of the final binary

```rust
// implicit static lifetime because 'static' keyword
static FOREVER: &str = "FOREVER";
// a static reference to a static string literal
let forever_ref: &'static str = &FOREVER;
// exactly the same thing
let forever: &'static str = "forever";
```

[📒](https://doc.rust-lang.org/1.17.0/book/lifetimes.html#static)