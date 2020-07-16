## advanced operators

```rust
let vec = vec![1, 2, 3, 4, 5];
let five = vec.iter()
    .take(3)
    .skip(1)
    .fold(0, |acc, it| acc + it);
let count = vec.iter().count();
let fifteen = vec.iter().sum();
let yes = vec.iter().any(|it| it % 2 == 0);
let thirty = vec.iter().chain(vec![5, 4, 3, 2, 1].iter()).sum();
```

* tip: use [itertools](https://crates.io/crates/itertools) for higher level operators