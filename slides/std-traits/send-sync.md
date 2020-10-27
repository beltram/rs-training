## [Send](https://doc.rust-lang.org/std/marker/trait.Send.html) & [Sync](https://doc.rust-lang.org/std/marker/trait.Sync.html)

* [Send](https://doc.rust-lang.org/std/marker/trait.Send.html) : allows transferring ownership between threads
* [Rc](https://doc.rust-lang.org/std/rc/struct.Rc.html) is not [Send](https://doc.rust-lang.org/std/marker/trait.Send.html),
[Arc](https://doc.rust-lang.org/std/sync/struct.Arc.html) is
* [Sync](https://doc.rust-lang.org/std/marker/trait.Sync.html) : allows accessing from multiple threads
* [Rc](https://doc.rust-lang.org/std/rc/struct.Rc.html) is not [Sync](https://doc.rust-lang.org/std/marker/trait.Sync.html),
[Mutex](https://doc.rust-lang.org/std/sync/struct.Mutex.html) is
* T is [Sync](https://doc.rust-lang.org/std/marker/trait.Sync.html) if &T is [Send](https://doc.rust-lang.org/std/marker/trait.Send.html)
* implementing [Send](https://doc.rust-lang.org/std/marker/trait.Send.html) or
[Sync](https://doc.rust-lang.org/std/marker/trait.Sync.html) yourself is considered unsafe

[📒](https://doc.rust-lang.org/book/ch16-04-extensible-concurrency-sync-and-send.html)