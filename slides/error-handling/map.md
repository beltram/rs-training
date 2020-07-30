## map()

* Maps an ``Option<T>``  to  ``Option<U>`` by applying a function to a contained value, leaving None value untouched
* Maps a ``Result<T, E>``  to  ``Result<U, E>`` by applying a function to a contained Ok value, leaving  Err value untouched

```rust
let none: Option<&str> = None;
let ok: Result<&str, &str> = Ok("abcde");
let fn_character_count = |s: &str| s.chars().count();
// Option<&str> -> Option<u32>
assert_eq!(Some("abcde").map(fn_character_count), Some(5)); 
assert_eq!(none.map(fn_character_count), None);
// Result<&str, &str> -> Result<u32, &str>
assert_eq!(ok.map(fn_character_count), Ok(5));
assert_eq!(Err("abcde").map(fn_character_count), Err("abcde"));
```


