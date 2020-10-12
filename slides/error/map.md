## .map()

* similar to Optional.map() in jvm languages
* `Option<T> --> Option<U>`
* `Result<T, E> --> Result<U, E>`

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

[📒](https://doc.rust-lang.org/std/option/enum.Option.html#method.map) | 
[📒](https://doc.rust-lang.org/std/result/enum.Result.html#method.map)