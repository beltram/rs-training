## HashSet operators

```rust
use std::{collections::HashSet, iter::FromIterator};

let a: HashSet<u8> = vec![1, 2, 3].into_iter().collect();
let b: HashSet<u8> = vec![2, 3, 4].into_iter().collect();
// union: all the unique elements in a & b
assert_eq!(vec![&1, &2, &3, &4], a.union(&b).collect::<Vec<&u8>>());
// difference: all the elements that are in a but not b
assert_eq!(vec![&1], a.difference(&b).collect::<Vec<&u8>>());
// intersection: all the elements that are only in a & b
assert_eq!(vec![&2, &3], a.intersection(&b).collect::<Vec<&u8>>());
// symmetric_difference: all the elements that are a or b, but not both
assert_eq!(vec![&1, &4], a.symmetric_difference(&b).collect::<Vec<&u8>>());
```

[📒](https://doc.rust-lang.org/stable/rust-by-example/std/hash/hashset.html) 