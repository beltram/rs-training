## combinator combination

* yes, the combinators can be... combined

```rust
Some("41")
  .ok_or("error message when None".to_string())// -> Result<&str, String>
  .or_else(|_| Ok("42"))// -> Result<&str, String>
  .and_then(|it| it.parse::<i32>().map_err(|e| e.to_string())) // -> Result<i32, String>
  .map_or(0, |n| 2 * n); // -> Result<i32, String>
```
[💻](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=d5349f4d3c770e56841ae29646198399)