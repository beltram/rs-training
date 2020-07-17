## HashSet

* 'HashSet<T>' is equivalent to 'HashMap<T, ()>'
* 'HashSet<T>' requires 'T' to implement [Eq](https://doc.rust-lang.org/std/cmp/trait.Eq.html) & [Hash](https://doc.rust-lang.org/std/hash/trait.Hash.html) traits
* HashSet guarantees uniqueness of its elements

```rust
use std::{collections::HashSet, iter::FromIterator};

let mut alphabet: HashSet<&str> = HashSet::new();
alphabet.insert("a"); // insertion
alphabet.insert("e");
let a: Option<&&str> = alphabet.get("a"); // safe access
let was_e_present: bool = alphabet.remove("e"); // delete & return true if present
// from a Vec
let departements: HashSet<u8> = vec![23, 75].into_iter().collect();
let departements: HashSet<u8> = HashSet::from_iter(vec![23, 75].into_iter());
```

[📒](https://doc.rust-lang.org/std/collections/struct.HashSet.html) | 
[📒](https://doc.rust-lang.org/stable/rust-by-example/std/hash/hashset.html) 