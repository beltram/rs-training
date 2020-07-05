## if is an expression

```rust
let a = if true { 1 } else { 0 };
// has to be exhaustive
let a = if true { 1 }; // ERROR
// arms must return same type
let a = if true { "true" } else { 0 }; // ERROR 
```

[📒](https://doc.rust-lang.org/1.7.0/book/if.html)