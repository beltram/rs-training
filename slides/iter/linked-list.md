## LinkedList

* Doubly-linked list, add/read at both ends
* Use only if you require it, Vec is always preferable

```rust
pub struct LinkedList<T> {
    head: Option<Node<T>>,
    tail: Option<Node<T>>,
    len: usize,
}
```

```rust
let mut primes: LinkedList<u8> = LinkedList::from_iter(vec![2, 3, 5, 7].into_iter());
let seven = primes.back(); // O(1)
primes.push_front(1); // O(1)
primes.push_back(11); // O(1)
```

[📒](https://doc.rust-lang.org/std/collections/struct.LinkedList.html)