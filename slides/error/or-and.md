## .or() / .and()

* works exactly like logical operators or, else and xor (nightly only)

```rust
let ok1: Result<&str, &str> = Ok("ok1");
let ok2: Result<&str, &str> = Ok("ok2");
let err1: Result<&str, &str> = Err("error1");
let err2: Result<&str, &str> = Err("error2");

assert_eq!(ok1.or(ok2), ok1);
assert_eq!(ok1.or(err1), ok1);
assert_eq!(err1.or(ok1), ok1);
assert_eq!(err1.or(err2), err2);

assert_eq!(ok1.and(ok2), ok2);
assert_eq!(ok1.and(err1), err1);
assert_eq!(err1.and(ok1), err1);
assert_eq!(err1.and(err2), err1);
```

[📒](https://learning-rust.github.io/docs/e6.combinators.html)