## slice

slice != array, slice are stack allocated, they are a reference to an array or vec section

```rust
let array = ["a", "b", "c", "d"];
let slice_a_b = &array[0..2];
let vec_slice = &vec![1, 2, 3][0..2];
// when omitted, lower bound is 0 & upper bound is len
let whole_array = &array[..];
// lower bound is inclusive, upper bound is exclusive
let slice_b_c = &array[1..3];
// notation for an inclusive upper bound
let slice_b_d = &array[1..=3];
```

[📒](https://doc.rust-lang.org/1.17.0/book/primitive-types.html#slices)