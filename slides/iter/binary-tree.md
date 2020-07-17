## Binary tree

* [BTreeMap](https://doc.rust-lang.org/std/collections/struct.BTreeMap.html) or [BTreeSet](https://doc.rust-lang.org/std/collections/struct.BTreeSet.html)
* each node has at most 2 children
* (left|right) child is (inferior|superior) to parent
* find an element in O(log2n)

```bash
                                 |5| <- node
                                /   \
         left child of '5' -> |3|   |6| <- right child of '5'
                             /  \    │
                           |2|  |4| |7|
```

[📒](https://en.wikipedia.org/wiki/Binary_tree)