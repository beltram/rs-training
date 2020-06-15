## Null safety

```rust
fn life() {
    let mut promoted: Option<bool> = Some(true);
    let promoted = promoted
        .map(|is_promoted| "Say 💩")
        .filter(|&said| said == "🙏")
        .and_then(|said| if said == "🙏" { Some("💰") } else { None })
        .or_else(|| Some("🔍 another 🏢"));
    if let Some(i_am_promoted) = promoted {
        println!("Hourra")
    }
}
```

[📒](https://doc.rust-lang.org/rust-by-example/std/option.html) | 
[💻](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=03b683232bd0411aeba8806d6d5b47d7)