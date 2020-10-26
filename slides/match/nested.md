## destructuring complex types

* destructuring allow breaking complex types into their components
* allows using component values separately from each other

```rust
let ((feet, inches), Point { x, y }) = ((3, 10), Point { x: 3, y: -10 });
```

[📒](https://doc.rust-lang.org/book/ch18-03-pattern-syntax.html#destructuring-structs-and-tuples)