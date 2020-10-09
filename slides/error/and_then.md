## and_then()

* Similar to flat_map in some other languages
* For Options: Return None if the option is None. Call a function with the wrapped value and returns the result
* For Result: Return Err(e) if the Result is Err. Call a function with the wrapped value and returns the result

```rust
// Example for Option
fn sq(x: u32) -> Option<u32> { Some(x * x) }
fn nope(_: u32) -> Option<u32> { None }

assert_eq!(Some(2).and_then(sq).and_then(sq), Some(16));
assert_eq!(Some(2).and_then(sq).and_then(nope), None);
assert_eq!(Some(2).and_then(nope).and_then(sq), None);
assert_eq!(None.and_then(sq).and_then(sq), None);
```