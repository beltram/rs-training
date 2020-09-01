## Useful crates

* To define more advanced custom Error types, check out [thiserror](https://docs.rs/thiserror/1.0.20/thiserror/) (good for libraries)
* For easy and idiomatic error handling, checkout [anyhow](https://docs.rs/anyhow/1.0.32/anyhow/) (good for binaries. Unit test may be harder)
    * Let you use the ? operator to propagate any error that implements std::error::Error trait
    * Highly recommended !!

```rust
use anyhow::Result;
// Result<T, anyhow::Error> and anyhow::Result<T> are equivalent
fn get_cluster_info() -> Result<ClusterMap> {
    // The 2 errors you can get from below are very different, but it works!
    let config = std::fs::read_to_string("cluster.json")?;
    let map: ClusterMap = serde_json::from_str(&config)?;
    Ok(map)
}
```