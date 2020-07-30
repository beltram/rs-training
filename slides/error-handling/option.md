## Option

```rust
struct Person {
  name: String,
  age: Option<u8>, // age is optional to define a Person
}
// Option can be used as return type for possible undefined behavior
// or easy error handling
fn is_adult(age: Option<u8>) -> Option<bool> { // age can be empty
    match age { //pattern matching on the Option
    Some(n) if n >= 18 => Some(true),
    Some(n) if n < 18 => Some(false),
    _ =>  None, // if age is empty we cannot give any answer
  }
}
```

[📒](https://doc.rust-lang.org/std/option/index.html)