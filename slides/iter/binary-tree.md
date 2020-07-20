## Binary tree

* [BTreeMap](https://doc.rust-lang.org/std/collections/struct.BTreeMap.html) or [BTreeSet](https://doc.rust-lang.org/std/collections/struct.BTreeSet.html)
* (left|right) child is (inferior|superior) to parent -> sorted collection
* add/find/remove an element in O(log2n)
* given `BTreeSet<K>` and `BTreeMap<K,V>`, 'K' has to implement [Ord](https://doc.rust-lang.org/std/cmp/trait.Ord.html) trait

```bash
                                 |5| <- node
                                /   \
         left child of '5' -> |3|   |6| <- right child of '5'
                             / │ \   │
                          |1||2||4| |7|
```

[📒](https://en.wikipedia.org/wiki/Binary_tree)