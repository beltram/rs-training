## infinite loop

* use 'break' to abort

```rust
let mut i = 0;
loop {
    if i > 10 {
        break;
    } else {
        i += 1;
    }
}
```

[📒](https://doc.rust-lang.org/1.17.0/book/loops.html)