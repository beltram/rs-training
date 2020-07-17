## Sized

* rustc requires ahead of time to know how much stack space it has to allocate for your program
* it will require arguments, methods returns and variables to be sized

```rust
fn unsized_arg(arr: [String]) {}
// ERROR              ^^^ doesn't have a size known at compile-time
fn sized_arg(arr: [String; 2]) {}

fn unsized_return() -> [String] { [String::new(), String::new()] }
// ERROR                 ^^^ doesn't have a size known at compile-time
fn sized_return() -> [String; 2] { [String::new(), String::new()] }

let unsized_var: [String] = [String::new(), String::new()];
// ERROR           ^^^ doesn't have a size known at compile-time
let sized_var: [String; 2] = [String::new(), String::new()];
```

[📒](https://doc.rust-lang.org/1.17.0/book/unsized-types.html)