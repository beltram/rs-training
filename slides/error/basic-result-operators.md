## basic Result operators

```rust
let ok: Result<i8, &str> = Ok(8);
let err: Result<i8, &str> = Err("Nope");

assert_eq!(ok.is_ok(), true);
assert_eq!(ok.is_err(), false);
// ok() : Result<T, E> --> Option<T>
assert_eq!(ok.ok(), Some(8));
assert_eq!(err.ok(), None);
// err() : Result<T, E> --> Option<E>
assert_eq!(ok.err(), None);
assert_eq!(err.err(), Some("Nope"));
```