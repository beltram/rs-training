## Move semantics: assignment

* variable bindings aka assignment takes ownership
* take ownership is commonly called moving
* prevents use after free (aka NPE), double-free error

```rust
let hello = String::from("Hello");
//  ----- move occurs because `hello` does not implement the `Copy` trait
let bonjour = hello;
//            ----- value moved here
println!("{} world !", hello);
//                     ^^^^^ value borrowed here after move
```

[📒](https://doc.rust-lang.org/1.17.0/book/ownership.html#move-semantics)