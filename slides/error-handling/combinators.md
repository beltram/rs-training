## Combinators

* We have different combinators which may be applied to Option and Result (we already saw ok_or/or_or_else)
* or(), and(), or_else() combine two values of type T and return same type T
* and_then(), apply a function on the Some/Ok value. Otherwise return None/Err. May change the type
* filter() only for Option, filter type T by using a closure. Return same type T
* map(), map_err(), convert type T with a closure. The return type may be changed
* map_or(), map_or_else()
    * convert type T with a closure
    * For None and Err, a default value or another closure is provided
* as_ref(), as_mut(), convert type T into a reference or mutable reference

[📒](https://learning-rust.github.io/docs/e6.combinators.html)