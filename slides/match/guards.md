## match guard

* A match guard is an additional if condition specified after the pattern in a match arm that must also match
* A new value is created inside the match expression. We don't use value from outside the expression

```rust
fn main() {
    let x = Some(5);
    let y = 10;
    match x {
// If we use Some(y) instead of Some(a) we would create an inner y value
        Some(a) if a < 4 => println!("Got small value"),
// As we don't define an inner y variable in the pattern above nor in that one
// (in the case described above we would always have n == y),
// we use the value from outer y variable and 5 != 10
        Some(n) if n == y => println!("Matched, n = {}", n), 
        _ => println!("Default case, x = {:?}", x), // arm selected
    }
    println!("at the end: x = {:?}, y = {}", x, y);
}
```

[📒](https://doc.rust-lang.org/book/ch18-03-pattern-syntax.html#extra-conditionals-with-match-guards)