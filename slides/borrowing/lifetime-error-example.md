## Lifetime by example


```rust
let trimmed: &str;
{
    let input = String::from("champion du monde");
    trimmed = trim_after(&input, "am");
    //                   ^^^^^^ borrowed value does not live long enough
} // <- 'input' dropped here and 'trimmed' still references it
println!("result: {}", trimmed);
//                     ------- borrow later used here
```

* without borrow checker & lifetimes
* println would have resulted in use after free