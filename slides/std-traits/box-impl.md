## [Box](https://doc.rust-lang.org/std/boxed/struct.Box.html)

```rust
// allocates a [u8;4] on the heap
let name: Box<str> = Box::from("abcd");
//        ^^^^^^^^ equivalent to &str

// access methods without dereferencing
assert_eq!(4, name.len());
// dereferencing required to access value
assert_eq!(*"abcd", *name);
```

[📒](https://doc.rust-lang.org/book/ch15-01-box.html)