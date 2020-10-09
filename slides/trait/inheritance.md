## inheritance

```rust
trait Vehicle {
    fn serial_id() -> &'static str;
}
trait Car: Vehicle {
    fn fuel() -> &'static str;
}
// trait Car: Vehicle + OtherTrait (for multiple inheritance)

struct MercedesBenz {}
impl Car for MercedesBenz {
    fn fuel() -> &'static str { "gasoline" }
}
impl Vehicle for MercedesBenz {
    fn serial_id() -> &'static str { "12345" }
}
```

[📒](https://doc.rust-lang.org/1.17.0/book/traits.html#inheritance)