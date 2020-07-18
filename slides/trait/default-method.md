## default method

* trait methods can declare default implementation
* can be overridden by implementer when declared explicitly 

```rust
trait Formula {
    fn is_installed(&self) -> bool;
    fn is_not_installed(&self) -> bool { !self.is_installed() }
}
```

[📒](https://doc.rust-lang.org/1.17.0/book/traits.html)