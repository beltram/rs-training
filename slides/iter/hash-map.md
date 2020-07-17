## HashMap

```rust
use std::{collections::HashMap, iter::FromIterator};

let mut alphabet: HashMap<u8, &str> = HashMap::new();
alphabet.insert(0, "a"); // insertion
alphabet.entry(4).or_insert("e"); // insert "e" if key 4 doesn't already exist
alphabet.entry(4).and_modify(|it| *it = "E"); // modify value if exists
let a: Option<&&str> = alphabet.get(&0); // safe access
let e: &str = alphabet[&4]; // unsafe access
let a: Option<&str> = alphabet.remove(&0); // delete & retrieve entry
// from a Vec
let departements: HashMap<u8, &str> = vec![(23, "Creuse")].into_iter().collect();
let departements: HashMap<u8, &str> = HashMap::from_iter(vec![(23, "Creuse")].into_iter());
```

[📒](https://doc.rust-lang.org/std/collections/struct.HashMap.html) 