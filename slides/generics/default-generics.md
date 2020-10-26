## default generics

* declare its default type after '='
* avoids redeclaration
* can be opted-out

```rust
trait Multiple<R = Self> { }
impl Multiple for u32 { } // 'R' is 'u32' 

trait SmallMultiple<R = u8> { }
impl SmallMultiple for u32 { } // 'R' is 'u8'
impl SmallMultiple<u16> for u64 { } // 'R' is 'u16'
```

[📒](https://doc.rust-lang.org/book/ch19-03-advanced-traits.html#default-generic-type-parameters-and-operator-overloading)