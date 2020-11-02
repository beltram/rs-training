## Cargo.toml

```toml
[dependencies] # <-- target
serde_json = "1.0.59"

[dependencies.serde] # <-- target
version = "1.0.117"
features = ["derive"]  # <-- for defining features

# built-in openssl version due to outdated version on osx, avoids linking issues
[target.'cfg(target_os = "macos")'.dependencies]
openssl = { version = "0.10.30", features = ["vendored"] }

[dev-dependencies] # <-- target
surf = "1.0.3"
```

[📒](https://doc.rust-lang.org/cargo/reference/manifest.html)