## .filter()

* only for Option

```rust
let is_even = |n: &i32| n % 2 == 0;

assert_eq!(None.filter(is_even), None);
assert_eq!(Some(3).filter(is_even), None);
assert_eq!(Some(4).filter(is_even), Some(4));
assert_eq!(Some(4).filter(|it| it % 2 == 0), Some(4));
```

[📒](https://doc.rust-lang.org/std/option/enum.Option.html#method.filter) 