## Composition over inheritance 

```rust
trait Automobile {
    fn drive() { println!("🚘") }
}
trait Plane { fn fly(); }
struct Twingo {}
impl Automobile for Twingo {}
```

[💻](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=4b52720a149d9506bf2bb76d6f3948f9)