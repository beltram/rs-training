## [Send](https://doc.rust-lang.org/std/marker/trait.Send.html) & [Sync](https://doc.rust-lang.org/std/marker/trait.Sync.html)

* Send : allows transferring ownership between threads
* Rc is not Send, Arc is
* Sync : allows accessing from multiple threads
* Rc is not Sync, Mutex is
* T is Sync if &T is Send
* implementing Send or Sync yourself is considered unsafe

[📒](https://doc.rust-lang.org/book/ch16-04-extensible-concurrency-sync-and-send.html)