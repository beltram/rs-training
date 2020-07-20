## function extension
```rust
trait Notifier {
    fn notify(&self);
}
impl Notifier for String {
    fn notify(&self) { println!("==> {:?}", self) }
}
impl Notifier for u8 {
    fn notify(&self) { println!("==> {:?}", self) }
}
fn main() {
    String::from("hello").notify();
    4.notify();
}
```

[📒](https://doc.rust-lang.org/1.17.0/book/traits.html)