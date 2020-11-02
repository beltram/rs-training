## tested snippets are preprocessed

* you may have noticed the code we saw earlier was not wrapped in a main function
* indeed, it would be painful to write this for each doctest and will lead to less clear documentation
* in fact, the code is preprocessed before its compilation
* one of the action is to wrap the code into a main function if it doesn't have one

[📒](https://doc.rust-lang.org/rustdoc/documentation-tests.html#pre-processing-examples)