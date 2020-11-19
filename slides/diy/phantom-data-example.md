## phantom data

* Example where a type T is associated with a struct but the struct actually don't own any T

```rust
use std::marker;

struct Vec<T> {
    data: *const T, // *const for variance!
    len: usize,
    cap: usize,
	// Will prevent the drop for that struct to behave like there is no T to drop
	// Allow drop check soundness 
    _marker: marker::PhantomData<T>,
}
```

[📒](https://doc.rust-lang.org/nomicon/phantom-data.html)