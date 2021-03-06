## .map_err()

* only for Result
* `Result<T, E> --> Result<T, F>`

```rust
// Very useful to handle several error type in the same function
let stringify = |x: u32| format!("error code: {}", x);

let x: Result<u32, u32> = Ok(2);
assert_eq!(x.map_err(stringify), Ok(2));

let x: Result<u32, u32> = Err(13);
assert_eq!(x.map_err(stringify), Err("error code: 13".to_string()));
```

[📒](https://doc.rust-lang.org/std/result/enum.Result.html#method.map_err)