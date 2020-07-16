## collecting

* iterators must be collected into a Vec (if required)
* similar to Java, unlike Kotlin

```rust
let vec = vec![1, 2, 3, 4, 5];
// declare resulting type explicitly
let even: Vec<&i32> = vec.iter()
    .filter(|&it| it % 2 == 0)
    .collect();
// or declare resulting type in collect::<>()
let odd = vec.iter()
    .filter(|&it| it % 2 != 0)
    .collect::<Vec<&i32>>();
```