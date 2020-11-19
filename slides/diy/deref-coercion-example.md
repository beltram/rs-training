## deref coercion

* Example

```rust
use std::rc::Rc;

fn foo(s: &str) { */omitted*/ }

// String implements Deref<Target=str>.
let owned = "Hello".to_string();
// Rc<T> type implements Deref<Target=T>
let counted = Rc::new(owned);

// &String will deref to &str
foo(&owned);
// &Rc<String> will deref to &String and then to &str. 
// Rust will do this as many time as possible until types match 
foo(&counted);
// Signature of foo didn't change but work with either types
```

