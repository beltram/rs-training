## iterating over String

* a String is a Vec<u8>
* slicing in a String only works for [ASCII](https://en.wikipedia.org/wiki/ASCII)
* panic occurs upon truncation in-between Unicode value
* tl;dr not recommended to iterate over a String by slicing

```rust
let hawk = String::from("hawk");
println!("'hawk' starts with a {}", &hawk[..1]);
let french_hawk = String::from("épervier");
println!("'épervier' starts with a {}", &french_hawk[..1]);
// panicked at 'byte index 1 is not a char boundary; it is inside 'é' (bytes 0..2) of `épervier`'
let chinese_hawk = String::from("鹰");
println!("'鹰' starts with a {}", &chinese_hawk[..1]);
// panicked at 'byte index 1 is not a char boundary; it is inside '鹰' (bytes 0..3) of `鹰`'
```
