## deref coercion

* The Deref trait in the std lib is normally used to overload *, the dereference operator
* Useful to write custom pointer types
* Special language feature linked to this trait: Deref coercion.  If you have a type U, and it implements `Deref<Target=T>`, values of &U will automatically coerce to a &T
	- One of the only places where Rust does an automatic conversion

[📒](https://doc.rust-lang.org/1.29.0/book/first-edition/deref-coercions.html)