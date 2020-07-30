## integers

```rust
let from_0_to_255: u8 = 0;
let from_minus_128_to_127: i8 = 0;
let default_i32 = 0;
let enforce_u8 = 42u8; // explicitly enforce type in declaration
let cast_to_u8 = 42 as u8; // or dynamically cast
let u64_on_64_proc: usize = 0;
// overflow fails in debug, not in release (no bound check)
let a: u8 = 255 + 1;
// won't compile because inferred type for integer is i32
let b = 2147483648;
//             ^ the literal `2147483648` does not fit into the type `i32` whose range is `-2147483648..=2147483647`
```

[📒](https://doc.rust-lang.org/1.17.0/book/primitive-types.html#numeric-types)