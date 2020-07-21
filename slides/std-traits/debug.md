## [Debug](https://doc.rust-lang.org/std/fmt/trait.Debug.html)

* for debugging context
* always use derive macro
* use with ':?' formatter or ':#?' for pretty printing

```rust
#[derive(Debug)]
struct Point { x: u8, y: u8 }
assert_eq!(
    "Point { x: 3, y: 9 }",
    format!("{:?}", Point { x: 3, y: 9 })
);
assert_eq!(
r#"Point {
    x: 3,
    y: 9,
}"#,
    format!("{:#?}", Point { x: 3, y: 9 })
);
```