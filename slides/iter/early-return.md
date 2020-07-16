## early return

* 'break' exists the loop
* 'continue' exists the current iteration and jumps to next
* both are not recommended

```rust
let mut i = 0;
loop {
    if i % 10 == 0 { break; }
    i += 1;
}
for j in 0..10 {
    if j % 2 == 1 { continue; }
    println!("{} is even", j);
}
```

[📒](https://doc.rust-lang.org/1.17.0/book/loops.html#ending-iteration-early)