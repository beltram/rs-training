## or() / and()

* This works exactly like logical operators or, else and xor (available on nightly)

```rust
let o1: Result<&str, &str> = Ok("ok1");
let o2: Result<&str, &str> = Ok("ok2");
let e1: Result<&str, &str> = Err("error1");
let e2: Result<&str, &str> = Err("error2");

assert_eq!(o1.or(o2), o1); // Ok1 or Ok2 = Ok1 // Some1 or Some2 = Some1
assert_eq!(o1.or(e1), o1); // Ok or Err = Ok // Some or None = Some
assert_eq!(e1.or(o1), o1); // Err or Ok = Ok // None or Some = Some
assert_eq!(e1.or(e2), e2); // Err1 or Err2 = Err2 // None1 or None2 = None2

assert_eq!(o1.and(o2), o2); // Ok1 and Ok2 = Ok2 // Some1 and Some2 = Some2
assert_eq!(o1.and(e1), e1); // Ok and Err = Err // Some and None = None
assert_eq!(e1.and(o1), e1); // Err and Ok = Err // None and Some = None
assert_eq!(e1.and(e2), e1); // Err1 and Err2 = Err1 // None1 and None2 = None1
```

[📒](https://learning-rust.github.io/docs/e6.combinators.html)