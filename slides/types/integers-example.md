## integers

```rust
let from_0_to_255: u8 = 0;
let from_minus_127_to_127: i8 = 0;
let default_i32 = 0;
let u64_on_64_proc: usize = 0;
// overflow fails in debug, not in release (no bound check)
let a: u8 = 255 + 1;
```

[📒](https://doc.rust-lang.org/1.7.0/book/primitive-types.html#numeric-types)