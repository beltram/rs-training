### destructuring complex types

* destructuring allow to break complex types into their components
* It allows to use component values separately from each other

```rust
let ((feet, inches), Point { x, y }) = ((3, 10), Point { x: 3, y: -10 });
```

[📒](https://doc.rust-lang.org/book/ch18-03-pattern-syntax.html#destructuring-structs-and-tuples)