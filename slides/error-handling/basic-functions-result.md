## Basic functions

* There are some basic function to test or transform Result

```rust
let result_ok: Result<i8, &str> = Ok(8);s
let result_err: Result<i8, &str> = Err("Nope");

assert_eq!(result_ok.is_ok(), true);
assert_eq!(result_ok.is_err(), false);
assert_eq!(result_ok.ok(), Some(8));       // transforms Ok(val) into Some(val)
assert_eq!(result_err.ok(), None);         // transforms Err(e) into None
assert_eq!(result_ok.err(), None);         // transforms Ok(val) into None
assert_eq!(result_err.err(), Some("Nope")) // transforms Err(e) into Some(e)
```