## Vec of u8 in memory

```rust
let vec: Vec<u8> = vec![0, 1, 2];
assert_eq!(24, std::mem::size_of_val(&vec));
```

```bash
          pointer
        /     length
      /     /     capacity
    /     /     /
+-----+-----+-----+
|  •  |  3  |  3  |
+--│--+-----+-----+
   │
+--V--+-----+-----+
|  0  |  1  |  2  |
+-----+-----+-----+
```

[📒](https://doc.rust-lang.org/1.17.0/book/vectors.html#vectors)