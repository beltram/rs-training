## .map_or_else()

* Same as map_or but fallback is lazy

```rust
// Option
assert_eq!(Some("foo").map_or_else(|| 2 * 31, |v| v.len()), 3);
//                                 ^^^^^^^^^ fallback
assert_eq!(None::<&str>.map_or_else(|| 2 * 31, |v| v.len()), 42);
//Result
let x: Result<_, &str> = Ok("foo");
assert_eq!(x.map_or_else(|e| 31 * 2, |v| v.len()), 3);
let x: Result<&str, _> = Err("bar");
assert_eq!(x.map_or_else(|e| 31 * 2, |v| v.len()), 42);
```