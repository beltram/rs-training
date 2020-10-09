## .iter()

* prefer '.iter()' over 'for' iteration
* equivalent to Java Stream Api

```rust
let mut vec = vec![1, 2, 3, 4, 5];
vec.iter().for_each(|i: &i32| {
    println!("A reference to {}", i)
});
vec.iter_mut().for_each(|i: &mut i32| {
    println!("A mutable reference to {}", i)
});
vec.into_iter().for_each(|i: i32| {
    println!("'into_iter' takes ownership of the vec and its element {}", i)
});
```