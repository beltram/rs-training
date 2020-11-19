## phantom data

* PhantomData is a special marker type
* It consumes no space, but simulates a field of the given type for static analysis
* Example where a lifetime is logically associated with a struct but not part of a field

```rust
use std::marker;
// Definition of Iter for &'a [T]
// Will logically contain a lot of &'a T and we need to "simulate" them
struct Iter<'a, T: 'a> {
    ptr: *const T,
    end: *const T,
	// Without this type, lifetime 'a would be unbounded
    _marker: marker::PhantomData<&'a T>,
}
```

[📒](https://doc.rust-lang.org/nomicon/phantom-data.html)