## function with enum
```rust
fn route(city: Workplace) -> () {} // Use of enum type in function signature
route(Workplace::Paris); // Call the function with Paris variant

enum Message { // each variant can have data with different type (you can even use struct or enum)
    Quit, // no data
    Move { x: i32, y: i32 }, // anonymous struct
    Write(String), // String
    ChangeColor(i32, i32, i32), // tuple struct
}

// All these data can be used with the same function signature
// in opposition of having 4 differents types
impl Message { // same impl as for a struct
	fn call(&self) {
		// snippet
	}
}

let m = Message::Write(String::from("hello"));
// we can enforce specific behavior directly from enum variant and its data
m.call(); 
```

[📒](https://doc.rust-lang.org/1.17.0/book/enums.html)
