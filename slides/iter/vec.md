## Vec<T>

* aka contiguous, growable array
* != java.util.ArrayList (not contiguous)

```rust
let mut vector = Vec::new();
// boring 😕
vector.push(0u8); // type of vector is inferred here
// vec! macro as a vararg alternative
let vec = vec![0, 1, 2];
// or init from an array
let vararg_vec = Vec::from([0, 1, 2]);
let vararg_vec: Vec<u8> = [0, 1, 2].into();
```

* consider [VecDeque](https://doc.rust-lang.org/std/collections/struct.VecDeque.html) if you need a queue.

[📒](https://doc.rust-lang.org/std/vec/struct.Vec.html) | 
[📒](https://doc.rust-lang.org/1.17.0/book/vectors.html#vectors)