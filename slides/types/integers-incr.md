## integers operators

* [no (pre|post)increment](https://github.com/dtolnay/rust-faq#why-doesnt-rust-have-increment-and-decrement-operators) like x++ or ++x
* variable has to be mutable

```rust
let mut i = 0;
i += 1; // shorthand
i = i + 1; // equivalent
i -= 1; // decrement
assert_eq!(i, 1);
let mut j = 2;
j *= 5; // multiply by
j *= j; // square
j /= 10; // divide by
assert_eq!(10, j);
```