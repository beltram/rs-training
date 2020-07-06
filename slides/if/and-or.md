## if operators

* '||' for OR
* '&&' for AND
* '^' for bitwise XOR

```rust
// OR
if a == 0 || a == 2 { println!("even") }
// AND
if a == 1 && b == 3 { println!("odd") }
// XOR () required
if (a == 1) ^ (b == 3) { println!("either 1 or 3") }
```

[📒](https://doc.rust-lang.org/1.17.0/book/if.html)