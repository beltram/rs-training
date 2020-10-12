## .or_else()

* defines a lazy fallback when Err or None
* Option closure has 0 argument, Err closure has 1

```rust
let ok: Result<&str, &str> = Ok("ok");
let err: Result<&str, &str> = Err("error");

// The closure must return the exact same type as the initial Result/Option
let fallback_ok = |_| -> Result<&str, &str> { Ok("also_ok") };
let fallback_err = |_| Err("also_error"); // closure return type omitted

assert_eq!(ok.or_else(fallback_ok), ok);
assert_eq!(ok.or_else(fallback_err), ok);
assert_eq!(err.or_else(fallback_ok), Ok("also_ok"));
assert_eq!(err.or_else(fallback_err), Err("also_error"));
```

[📒](https://doc.rust-lang.org/std/option/enum.Option.html#method.or_else) | 
[📒](https://doc.rust-lang.org/std/result/enum.Result.html#method.or_else) | 
[📒](https://learning-rust.github.io/docs/e6.combinators.html#or-else)