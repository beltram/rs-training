## Standard traits
* Copy, Clone: I can be deep copied [📒](https://doc.rust-lang.org/std/marker/trait.Copy.html#whats-the-difference-between-copy-and-clone)
* Display: I can be printed in println!("{}", dis) without formatter like {:?} [📒](https://doc.rust-lang.org/std/fmt/trait.Display.html)
* (De)Serializable: From serde (marshalling) [📒](https://docs.serde.rs/serde/trait.Serialize.html)
* Debug: Destructure structs fields while printed [📒](https://doc.rust-lang.org/std/fmt/trait.Debug.html)
* Send: Type can be sent to another thread (automatic derived, no impl) [📒](https://doc.rust-lang.org/std/marker/trait.Send.html)
* Sync: Type can be shared between threads (automatic derived, no impl) [📒](https://doc.rust-lang.org/std/marker/trait.Sync.html)