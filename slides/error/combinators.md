## combinators

* different combinators may be applied to Option and Result
* or(), and(), or_else() combine two values of type T and return same type T
* and_then() similar to flat_map()
* filter() (Option only)
* map() for altering
* map_err() alters Err e.g. contextualize error message
* map_or(), map_or_else() for altering or continue with a fallback
* as_ref(), as_mut(), convert type T into a reference or mutable reference

[📒](https://learning-rust.github.io/docs/e6.combinators.html)