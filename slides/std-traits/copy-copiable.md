## can my struct implement [Copy](https://doc.rust-lang.org/std/marker/trait.Copy.html) ?

* all types MUST implement copy
* NO mutable borrow

```rust
#[derive(Copy, Clone)]
struct NotCopiable<'a> {
    a_string: String,
    a_vec: Vec<u8>,
    a_mutable_ref: &'a mut u8,
    another_not_copiable_struct: NotCopiable<'a>,
}
```

[📒](https://doc.rust-lang.org/std/marker/trait.Copy.html#when-can-my-type-be-copy)