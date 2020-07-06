## array

arrays have a fixed size, are immutable by default, are zero indexed 👍

```rust
let array: [u8; 3] = [1, 2, 3];
// notation [T; N] where T is elements type & N number of elements
let array_are_sized: [u8; 5] = [1, 2, 3, 4, 5];
let array_type_inference = [1, 2, 3]; // type is [u8; 3]
let array_of_str: [&str; 2] = ["a", "b"]
// accessors
let array_len = array.len();
let one = array[0];
// mutable array
let mut mut_array = ["a", "b", "c"];
mut_array[0] = "z";
// shorthand for initializing an array and filling it
let array_containing_1_ten_times = [1; 10];
```
[📒](https://doc.rust-lang.org/1.17.0/book/primitive-types.html#arrays)