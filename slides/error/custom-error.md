## Custom Error Type

* It is possible to create your own Error types
* Useful to handle your own error cases but also to convert other Error types. It is sometimes easier to handle only one error type in a function
* It is recommended to implement the std::error::Error trait when defining an Error (requires Debug and Display traits), but this is not mandatory
* Let's see an example in the next two slides

[📒](https://doc.rust-lang.org/stable/rust-by-example/error/multiple_error_types/define_error_type.html)
[📒](https://doc.rust-lang.org/std/error/trait.Error.html)