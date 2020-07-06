## tuple struct

* aka 'zero cost abstraction'
* inlined as tuple by compiler
* use it for expressiveness e.g. 'struct Seconds(u8);'

```rust
struct IpV4Addr(u8, u8, u8, u8);
let localhost = IpV4Addr(127, 0, 0, 1);
let IpV4Addr(a, b, c, d) = localhost; // destructure like this
let a = localhost.0; // access fields by zero indexed accessors
```

[📒](https://doc.rust-lang.org/1.17.0/book/structs.html#tuple-structs)