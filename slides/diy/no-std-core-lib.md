## no-std & core lib

The [core lib](https://doc.rust-lang.org/core/) is a set of portable primitives. Does not rely on operating system librairies. (e.g. *libc*)


[#!\[no_std\]](https://rust-embedded.github.io/book/intro/no-std.html) is a crate-level attribute that indicates that the crate will link to the *core-crate* instead of the *std-crate*.

<img src="lib/images/no-std.png" style="height:30vh"/>