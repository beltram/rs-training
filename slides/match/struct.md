## destructuring structs
* Ranges are only allowed with numeric values & chars (compiler check the range is not empty at compile time)

```rust
struct Point {
    x: i32,
    y: i32,
}
fn main() {
    let p = Point { x: 0, y: 7 };
    // The 2 below are stricly equivalent
    let Point { x: a, y: b } = p;
    assert_eq!(0, a);
    assert_eq!(7, b);

    let Point { x, y } = p;
    assert_eq!(0, x);
    assert_eq!(7, y);
}
```

[📒](https://doc.rust-lang.org/book/ch18-03-pattern-syntax.html#destructuring-structs)