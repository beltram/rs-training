## match guard

* is an additional 'if' condition specified after the pattern in a match arm that must also match
* a new binding is created inside the match expression
* pay attention to new binding name to avoid  shadowing outer bindings

```rust
let x = Some(5);
let y = 10;
match x {
    // if we use 'Some(y)' instead of 'Some(a)' we would create a 'y' binding
    Some(a) if a < 4 => println!("Got small value"),
    // 'n' cannot be named 'y' otherwise would shadow the outer 'y'
    Some(n) if n == y => println!("Matched, n = {}", n),
    _ => println!("Default case, x = {:?}", x),
}
```

[📒](https://doc.rust-lang.org/book/ch18-03-pattern-syntax.html#extra-conditionals-with-match-guards)