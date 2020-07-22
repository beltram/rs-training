## function parameter

* fn foo(PATTERN: TYPE) {}
* function parameters take only [irrefutable](https://doc.rust-lang.org/book/ch18-02-refutability.html) patterns

```rust
fn foo(x: i32) {} // the x part is a pattern

fn print_coordinates(&(x, y): &(i32, i32)) {
    println!("Current location: ({}, {})", x, y);
}

fn main() {
    let point = (3, 5);
    print_coordinates(&point); // &point reference can be destructure as &(3, 5)
}
```

[📒](https://doc.rust-lang.org/book/ch18-01-all-the-places-for-patterns.html#function-parameters)