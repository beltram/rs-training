## map_or_else()

* Same as map_or but use a fallback function instead of a default value

```rust
// Option
let k = 21;
let x = Some("foo");
// First function (here a closure) is for the default value and takes 0 arg
// Second function takes 1 arg
assert_eq!(x.map_or_else(|| 2 * k, |v| v.len()), 3);
let x: Option<&str> = None;
assert_eq!(x.map_or_else(|| 2 * k, |v| v.len()), 42);
//Result
let x : Result<_, &str> = Ok("foo");
assert_eq!(x.map_or_else(|e| k * 2, |v| v.len()), 3);
let x : Result<&str, _> = Err("bar");
assert_eq!(x.map_or_else(|e| k * 2, |v| v.len()), 42);
```