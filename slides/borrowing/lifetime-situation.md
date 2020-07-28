## Lifetime situation

* my function returns a reference
* cannot be a reference to something created inside the function because dropped when function ends
* so return has to be a reference to one of the args

```rust
/// returns string slice after first occurrence of prefix
fn trim_after(from: &str, prefix: &str) -> &str {
    let idx = from.find(prefix)
        .map(|it| it + prefix.len())
        .unwrap_or_else(|| 0);
    &from[idx..]
}
```

* but which one ? rustc does not evaluates my function body
* I need to make sure that when variable referenced by 'from' will be dropped
* my return won't be used ! Otherwise use after free