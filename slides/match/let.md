## let

* 'let x = 5' <==> 'let PATTERN = EXPRESSION'
* let statements take only [irrefutable](https://doc.rust-lang.org/book/ch18-02-refutability.html) patterns

```rust
let (x, y, z) = (1, 2, 3); // destructure a tuple
assert_eq!(y, 2);
let (x, _, z) = (1, 2, 3); // ignore second value
let (first, ..) = (3,20,4,107,223,9);
let (.., last) = (3,20,4,107,223,9);

let (x, y) = (1, 2, 3); // compile error, not irrefutable
```

[📒](https://doc.rust-lang.org/book/ch18-01-all-the-places-for-patterns.html#let-statements)