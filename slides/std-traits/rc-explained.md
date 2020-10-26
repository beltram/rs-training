## [Rc](https://doc.rust-lang.org/std/rc/struct.Rc.html)

* keeps track of the number of references to a value still in use
* has an internal counter which is
    * incremented when '.clone()'
    * decremented when '.drop()'
* when counter is 0, the value is dropped for good

[📒](https://doc.rust-lang.org/book/ch15-04-rc.html)