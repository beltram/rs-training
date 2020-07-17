## Unsized

* BUT unsized types are allowed on:
    * trait implementation
    * last field of a struct

```rust
trait Hello {}
// unsized implementing trait
impl Hello for [String] {}

// only last field of a struct can be unsized
struct OneUnsized {
    first_sized: String,
    other_also_sized: String,
    last_unsized: [String],
}
```

[📒](https://doc.rust-lang.org/1.17.0/book/unsized-types.html)