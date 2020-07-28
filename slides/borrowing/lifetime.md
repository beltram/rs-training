## Lifetime

* Rust wants to prevent use after free
* We are lending references to other blocks
* How to make sure other blocks always access valid references ?

```rust
// use after free example
let y: &i32;
{
    let x = 5;
    y = &x;
    //  ^^ borrowed value does not live long enough
} // <- 'x' dropped here while still borrowed 
println!("{}", y);
//             - borrow later used here
```

[📒](https://doc.rust-lang.org/1.17.0/book/lifetimes.html)