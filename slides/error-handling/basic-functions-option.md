## Basic functions

* There are some basic function to test or transform Option

```rust
let opt_some: Option<u8> = Some(8);
let opt_none: Option<u8> = None;

assert_eq!(opt_some.is_some(), true);
assert_eq!(opt_some.is_none(), false);
assert_eq!(opt_some.ok_or("This is an error"), Ok(8));
assert_eq!(opt_none.ok_or("This is an error"), Err("This is an error"));
assert_eq!(opt_some.ok_or_else(|| "Another error"), Ok(8));
assert_eq!(opt_none.ok_or_else(|| "Another error"), Err("Another error"));  
```