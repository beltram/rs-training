## Custom Error Type

```rust
// Following snippet on previous slide
use std::fs::File;
use std::io;

fn main() -> Result<(), AppError> {
// This will generates an io::Error. But because of return type is 
// Result<(), AppError>, it converts to AppError
  let _file = File::open("nonexistent_file.txt")?;
// Or explicitely: we use map_err to convert io::Error into AppError.
// Possible thanks to From implementation
  let _file = File::open("nonexistent_file.txt").map_err(|e| AppError::from(e));
  println!("{:?}", _file);
  Ok(())
}
```

[💻](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=2c779817f9bd6c4a179ab43779c963ef)