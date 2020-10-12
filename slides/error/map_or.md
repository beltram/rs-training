## .map_or()

* map or fallback
* eager ! Prefer lazy '.map_or_else()'

```rust
// Option
assert_eq!(Some("foo").map_or(42, |it| it.len()), 3);
assert_eq!(None::<&str>.map_or(42, |v| v.len()), 42);

//Result
let x: Result<_, &str> = Ok("foo");
assert_eq!(x.map_or(42, |v| v.len()), 3);
let x: Result<&str, _> = Err("bar");
assert_eq!(x.map_or(42, |v| v.len()), 42);
```

[📒](https://doc.rust-lang.org/std/option/enum.Option.html#method.map_or) | 
[📒](https://doc.rust-lang.org/std/result/enum.Result.html#method.map_or)