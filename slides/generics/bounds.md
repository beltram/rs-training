## bounds

* bound has to be a trait, not a struct

```rust
trait Human { }

fn find_parent<T: Human>(of: T) -> T { }

fn print_human<T: Human + Display>(of: T) {
    println!("Human {}", of)
}
```

[📒](https://doc.rust-lang.org/stable/rust-by-example/generics/bounds.html)