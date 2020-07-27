## float

|  Type   | 32-bit | 64-bit   |
|:-------:|:------:|:--------:|
|  float  |   f32  |    f64  |

```rust
let float = 1.0;
let float: f32 = 1.0;
let float: f64 = 1.0;
let default_f64 = 1.0;
let enforce_f32 = 1.0f32;
```

* As always, float comparison can be tricky. See this [crate](https://crates.io/crates/float-cmp)

* To represent monetary amounts use [bigdecimal](https://crates.io/crates/bigdecimal) crate

[📒](https://doc.rust-lang.org/1.17.0/book/primitive-types.html#numeric-types)