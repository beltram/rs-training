## char

* a single [Unicode](https://en.wikipedia.org/wiki/Unicode) value (full list [here](https://en.wikipedia.org/wiki/List_of_Unicode_characters))
* represented by 4 bytes in memory
* declare between single quotes ''

```rust
assert_eq!(4, std::mem::size_of::<char>()); // 4 bytes
let a: char = 'a';
let b = 'b'; // type inference
let emoji = '💕'; // can represent single code point Unicode emojis
```

[📒](https://doc.rust-lang.org/1.17.0/book/primitive-types.html#char) | 
[📒](https://doc.rust-lang.org/1.17.0/std/primitive.char.html) 