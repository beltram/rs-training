## Macro

for code inside block, use macro form cfg!()

```rust
#![allow(unused)]

fn main() {
    let machine_kind = if cfg!(unix) {
        "unix"
    } else if cfg!(windows) {
        "windows"
    } else {
        "unknown"
    };

    println!("I'm running on a {} machine!", machine_kind);
}
```
