## let

* let x = 5 <==> let PATTERN = EXPRESSION
* let statements take only [irrefutable](https://doc.rust-lang.org/book/ch18-02-refutability.html) patterns

```rust
let (x, y, z) = (1, 2, 3); // destructure the tuple
assert_eq!(y, 2);
let (x, y) = (1, 2, 3); // Compile ERROR
let (x, _, z) = (1, 2, 3); // Throw away the second value
let (x, ..) = (3,20,4,107,223,9); // Throw away all values except the first
```

[📒](https://doc.rust-lang.org/book/ch18-01-all-the-places-for-patterns.html#let-statements)