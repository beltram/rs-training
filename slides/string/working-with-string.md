## in practice

```rust
let a_string_from: String = String::from("hello");
let literal_to_string: String = "hello".to_string(); // exactly the same
let new_string: String = String::new(); // no heap allocated
let default_string: String = String::default(); // same as String::new()
let mut growable_string = String::from("hello");
growable_string.push_str("world"); // growable
// string concatenation
let (a, b) = (String::from("a"), String::from("b"));
// prefer format! macro for string concatenation
let c = format!("{}{}", &a, &b);
// concatenation with + takes ownership of left member
let c = a + &b; // here a is owned, b borrowed
println!("{}", a); // ERROR
//             ^ value borrowed here after move
```