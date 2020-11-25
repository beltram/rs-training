## lifetime elision rules
* If there is exactly one input lifetime position (elided or not), that lifetime is assigned to all elided output lifetimes.

```rust
fn substr(s: &str, until: usize) -> &str;               // elided
fn substr<'a>(s: &'a str, until: usize) -> &'a str;     // expanded

fn new(buf: &mut [u8]) -> BufWriter;                    // elided
fn new<'a>(buf: &'a mut [u8]) -> BufWriter<'a>          // expanded
```
