## Cargo
Cargo.toml
```
[package]
name = "sample"
version = "0.0.1"
authors = ["beltram.maldant"]

[dependencies]
clap = "2.33.0"

[dev-dependencies]
spectral = "0.6.0"

[profile.release]
opt-level = 'z'  # Optimize for size.
```
[toml reference](https://github.com/toml-lang/toml/wiki)