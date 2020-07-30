## map_err()

* Only available for Result
* Maps a ``Result<T, E>`` to ``Result<T, F>`` by applying a function to a contained Err value, leaving an Ok value untouched

```rust
// Usually very useful to handle several error type in the same function
// Very basic usage below
fn stringify(x: u32) -> String { format!("error code: {}", x) }

fn main() {
    let x: Result<u32, u32> = Ok(2);
    assert_eq!(x.map_err(stringify), Ok(2));

    let x: Result<u32, u32> = Err(13);
    assert_eq!(x.map_err(stringify), Err("error code: 13".to_string()));
}
```