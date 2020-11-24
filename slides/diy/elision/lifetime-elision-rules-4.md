## lifetime elision rules
* Otherwise, it is an error to elide an output lifetime.
```rust
fn get_str() -> &str;                                   // ILLEGAL, no inputs to infer from
fn frob(s: &str, t: &str) -> &str;                      // ILLEGAL, cannot know whether to use first or second lifetime
```
