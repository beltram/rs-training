## Option & Result

* Rust doesn't have null, we use Option for that
    * Option stands for optional value. It can be 'Some(value)' or 'None'
* Rust don't have Exceptions, we use Result for that
    * Result can represent success 'Ok(value)' or failure 'Err(error)'
* Both are <a href="#/8/1">enums</a>. We can use <a href="#/8/6">pattern matching</a> on them. Guarantees exhaustiveness
* Both are in prelude. No need to import, namespace them (e.g. 'std::option::Option')

[📒](https://doc.rust-lang.org/1.17.0/book/error-handling.html#the-option-type)
[📒](https://doc.rust-lang.org/1.17.0/book/error-handling.html#the-result-type)