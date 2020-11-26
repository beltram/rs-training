## Async bases
* based upon standard feature: async/await
* usually, these runtime bring 1 reactor, and n executors
    * reactor = way to subscribe to events (timer, I/O, ...)
    * executor = schedule and execute tasks (keep track of what is waiting, wake up, ...)

[📒](https://rust-lang.github.io/async-book/01_getting_started/01_chapter.html)