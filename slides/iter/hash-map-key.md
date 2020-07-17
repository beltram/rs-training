## HashMap keys

* a key MUST implement [Eq](https://doc.rust-lang.org/std/cmp/trait.Eq.html) & [Hash](https://doc.rust-lang.org/std/hash/trait.Hash.html) traits
* std types already satisfying those conditions: 
    * [bool](https://doc.rust-lang.org/std/primitive.bool.html), integers (signed or not) e.g. u8, i32 etc..
    * [String](https://doc.rust-lang.org/std/string/struct.String.html) and [&str](https://doc.rust-lang.org/std/primitive.str.html)

```rust
use std::collections::HashMap;

#[derive(Eq, PartialEq, Hash)]
struct Person { firstname: String, lastname: String, }

let mut nicknames: HashMap<Person, &str> = HashMap::new();
let beltram = Person { firstname: String::from("beltram"), lastname: String::from("maldant") };
nicknames.insert(beltram, "trambel");
```

[📒](https://doc.rust-lang.org/stable/rust-by-example/std/hash/alt_key_types.html) | 
[📒](https://doc.rust-lang.org/stable/rust-by-example/std/hash.html)
