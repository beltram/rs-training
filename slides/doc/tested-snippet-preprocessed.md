## tested snippets are preprocessed

* As you may have noticed the code we saw earlier was not wrapped in any main function
* Indeed, it would be painfull to write this for each doctest and will lead to less clear documentation
* In fact the code is preprocessed before its compilation
* One of the action is to wrapp the code into a main fucntion if it doesn't have one. See below link for more details

[📒](https://doc.rust-lang.org/rustdoc/documentation-tests.html#pre-processing-examples)