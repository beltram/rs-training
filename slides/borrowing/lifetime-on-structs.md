## lifetime on structs

* named lifetime required on struct declaration
* named lifetime can/must be declared in impl blocks

```rust
struct Person<'a> {
    firstname: &'a str
}

impl<'a> Person<'a> {
    fn get_name(&self) -> &'a str { self.firstname }
    fn local_lifetime<'b>(&'b self) -> &'b str { self.firstname }
}

impl<'a> Default for Person<'a> {
    fn default() -> Self { Self { firstname: "" } }
}
```

[📒](https://doc.rust-lang.org/1.17.0/book/lifetimes.html#in-structs)