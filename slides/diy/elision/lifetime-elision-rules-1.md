## lifetime elision rules
*  Each elided lifetime in input position becomes a distinct lifetime parameter.
```rust
fn print(s: &str);                                      // elided
fn print<'a>(s: &'a str);                               // expanded
```
