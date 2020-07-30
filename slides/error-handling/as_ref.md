## as_ref() / as_mut()

* as_ref() : Convert `Option<T>` to `Option<&T>` and `Result<T, E>` to `Result<&T, &E>`
    * May aussi take a `&Option<T>` or `&Result<T, E>` (same return type)
* as_mut() : Converts `Option<T>` to `Option<&mut T>` and `Result<T, E>` to `Result<&mut T, &mut E>`
    * May aussi take a `&mut Option<T>` or `&mut Result<T, E>` (same return type)
