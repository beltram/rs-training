## Filter

* Available only for option
* Returns None if the option is None, otherwise calls predicate with the wrapped value and returns:
    * Some(value) if predicate returns true
    * None if predicate returns false

```rust
fn is_even(n: &i32) -> bool {
    n % 2 == 0
}

assert_eq!(None.filter(is_even), None);
assert_eq!(Some(3).filter(is_even), None);
assert_eq!(Some(4).filter(is_even), Some(4));
assert_eq!(Some(4).filter(|it| it % 2 == 0), Some(4));
```