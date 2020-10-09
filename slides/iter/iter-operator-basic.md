## most common operators

```rust
vec![1, 2, 3, 4, 5].iter()
    .map(|it| it + 1)
    .filter(|&it| it > 3)
    .flat_map(|it| vec![0, it])
    .for_each(|it| println!("{}", it));
```