## orphan rule

* The `overlap rules`: You can't write two impl blocks that "overlap", i.e. apply to some of the same types. 
    - For example, `impl<T: Debug>` Trait for T overlaps with `impl<T: Display>` Trait for T because some types might implement both
* The `orphan rules` forbid you from writing an impl where both the trait and the type are defined in a different crate.
	- Prevent dependency problem where multiple crates write conflicting impls on the same type (meaning we can't use both crates in the same project)
	- Allow crates to add impls for their traits and types without it being considered a breaking change


[📒](https://github.com/Ixrec/rust-orphan-rules#:~:text=The%20%22orphan%20rules%22%2C%20very,This%20is%20meant%20to%3A&text=Allow%20crates%20to%20add%20impl,being%20considered%20a%20breaking%20change)
