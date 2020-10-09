## basic Option operators 

```rust
let some: Option<u8> = Some(8);
let none: Option<u8> = None;

assert_eq!(some.is_some(), true);
assert_eq!(some.is_none(), false);
assert_eq!(some.ok_or("This is an error"), Ok(8));
assert_eq!(none.ok_or("This is an error"), Err("This is an error"));
assert_eq!(some.ok_or_else(|| "Another error"), Ok(8));
assert_eq!(none.ok_or_else(|| "Another error"), Err("Another error"));  
```