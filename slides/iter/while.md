## while

```rust
let mut i = 0;
let mut done = false;
while !done {
    i += 1;
    done = i % 10 == 0;
}
```

[📒](https://doc.rust-lang.org/1.17.0/book/loops.html#while)