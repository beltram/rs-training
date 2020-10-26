## pitfall

* as anything creating a binding, it introduces shadowing

```rust
let x = 1;
let c = 'c';

match c {
    x => println!("x: {}, c: {}", x, c), // prints 'x: c, c: c'
}

println!("x: {}", x) // prints 'x: 1'
```

[📒](https://doc.rust-lang.org/1.17.0/book/patterns.html)