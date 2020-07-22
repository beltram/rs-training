## pitfall

* As anything creating a binding, it introduces shadowing

```rust
let x = 1;
let c = 'c';

match c {
    x => println!("x: {} c: {}", x, c), // this will print x: c c: c
}

println!("x: {}", x) // this will print x: 1
```

* We'll now see all the places where we can use patterns

[📒](https://doc.rust-lang.org/1.17.0/book/patterns.html)