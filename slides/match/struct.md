## destructuring structs

* Structs can be destructured using the way the data is stored within the struct

```rust
struct Point {
    x: i32,
    y: i32,
}
let p = Point { x: 0, y: 7 };
// both syntaxes below are strictly equivalent
let Point { x: a, y: b } = p;
assert_eq!(0, a);
assert_eq!(7, b);

let Point { x, y } = p; // x and y must match struct definition
assert_eq!(0, x);
assert_eq!(7, y);
```

[📒](https://doc.rust-lang.org/book/ch18-03-pattern-syntax.html#destructuring-structs)