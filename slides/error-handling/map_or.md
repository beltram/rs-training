## map_or()

* Option: Applies a function to the contained value (if any), or returns the provided default (if not)
* Result: Applies a function to the contained value (if Ok), or returns the provided default (if Err)
* Arguments passed to map_or are always evaluated. If you pass the result of a function call, you should prefer map_or_else which is lazy

```rust
// Option
let x = Some("foo");
assert_eq!(x.map_or(42, |v| v.len()), 3);
let x: Option<&str> = None;
assert_eq!(x.map_or(42, |v| v.len()), 42);
//Result
let x: Result<_, &str> = Ok("foo");
assert_eq!(x.map_or(42, |v| v.len()), 3);
let x: Result<&str, _> = Err("bar");
assert_eq!(x.map_or(42, |v| v.len()), 42);
```