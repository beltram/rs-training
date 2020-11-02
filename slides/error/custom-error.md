## custom Error type

* you can create your own Error types
* for
  * defining custom errors your crate might throw
  * abstracting other external error types
* it is easier to handle only one error type in a function
* recommended to implement 'std::error::Error' trait when defining an Error, but not mandatory

[📒](https://doc.rust-lang.org/stable/rust-by-example/error/multiple_error_types/define_error_type.html)
[📒](https://doc.rust-lang.org/std/error/trait.Error.html)