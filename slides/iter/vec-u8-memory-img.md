## Vec of u8 in memory

```rust
let vec: Vec<u8> = vec![9, 8, 7];
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
|  9  |  8  |  7  |
+-----+-----+-----+
```

[📒](https://doc.rust-lang.org/1.17.0/book/vectors.html#vectors)