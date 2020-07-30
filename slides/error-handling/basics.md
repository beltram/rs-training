# Basics

* rust don't have any implementation for null, we use Option for that
    * Option stand for optional value. It can have Some(value) or None (no value)
* rust don't have any implementation for Exceptions, we use Result for that
    * Result can represent success with Ok(value) or failure with Err(error)
* Option and Result are <a href="#/6/5">enum</a> so we can use pattern matching on them and the compiler can always make sure all cases are covered
* Option and Result are in prelude so you don't need to namespace them to use them (like std::option::Option)


[📒](https://doc.rust-lang.org/1.17.0/book/error-handling.html#the-option-type)
[📒](https://doc.rust-lang.org/1.17.0/book/error-handling.html#the-result-type)