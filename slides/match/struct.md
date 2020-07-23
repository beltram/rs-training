## destructuring structs
* Structs can be destructured using the way the data is stored within the strcut

```rust
struct Point {
    x: i32,
    y: i32,
}
fn main() {
    let p = Point { x: 0, y: 7 };
    // The 2 syntaxs below are stricly equivalent
    let Point { x: a, y: b } = p;
    assert_eq!(0, a);
    assert_eq!(7, b);

    let Point { x, y } = p; // x and y must match with struct definition
    assert_eq!(0, x);
    assert_eq!(7, y);
}
```

[📒](https://doc.rust-lang.org/book/ch18-03-pattern-syntax.html#destructuring-structs)