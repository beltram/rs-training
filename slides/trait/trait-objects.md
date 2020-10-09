## Trait objects

* in order to perform dynamic dispatch, Formula trait need to be a 'Trait Object'
* in order for a trait to be a 'Trait Object' it has to be 'Object Safe'
---
* the trait is 'Object Safe' if
    * it MUST NOT require that 'Self : Sized'
    * all of its methods are 'Object Safe'
* all its methods MUST require that 'Self : Sized' ... or:
    * MUST NOT have any type parameter (<T>)
    * MUST NOT use 'Self'

[📒](https://doc.rust-lang.org/1.17.0/book/trait-objects.html#object-safety)