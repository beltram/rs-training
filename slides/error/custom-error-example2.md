## custom Error type

```rust
use std::fs::File;
use std::io;

fn main() -> Result<(), AppError> {
    // 2 different ways to map 'io::Error' to 'AppError'
    let file = File::open("nonexistent_file.txt")?;
    //                  implicit conversion here ^
    let file = File::open("nonexistent_file.txt")
        .map_err(|e| AppError::from(e)); // <-- explicit conversion
    Ok(())
}
```