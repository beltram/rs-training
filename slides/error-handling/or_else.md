## or_else()

* if the Option is Some(val) return Some(val). Return the result of the closure if None
* if the Result is Ok(val) return Ok(vam). Return the result of the closure if Err(e)
* The only difference is that the closure should have 0 argument for Option and 1 for Result

```rust
//We'll see a subset of previous examples with Result to understand
let ok: Result<&str, &str> = Ok("ok1");
// The closure must return the exact same type than the initial Result/Option
let fn_ok = |_| -> Result<&str, &str> { Ok("ok2") };
let err: Result<&str, &str> = Err("error1");
let fn_err = |_| Err("error2"); // closure return type omitted
assert_eq!(ok.or_else(fn_ok), ok);
assert_eq!(ok.or_else(fn_err), ok);
// Err("error1") is overrrided by the result of the closure fn_ok
assert_eq!(err.or_else(fn_ok), Ok("ok2"));
// Err("error1") is overrrided by the result of the closure fn_err
assert_eq!(err.or_else(fn_err), Err("error2")); 
```

[📒](https://learning-rust.github.io/docs/e6.combinators.html#or-else)