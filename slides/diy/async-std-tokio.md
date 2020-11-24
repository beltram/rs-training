## async-std or tokio
* based upon standard feature: async/await
* usually, these runtime bring 1 reactor, and n executors
    * reactor = way to subscribe to events (timer, I/O, ...)
    * executor = schedule and execute tasks (keep track of what is waiting, wake up, ...)
* futures crate
    * traits and functions to do async
    * has an executor, but no reactor (so no timer or async IOs)
    * might be included in std at some point
    * Futures need to be polled to completion. This is the job of an executor. Some futures additionally need to wait for events from the kernel to know when there might be data ready to read from a file, or somesuch. A reactor handles this
    * is used by smol and async-std
* Three main "crates" to handle async:
    * tokio = ecosystem with HTTP/gRPC/tracing implem
    * async-std = aync way to use std components
    * smol = simplified async runtime
* async-std and smol:
    * use the same reactor/executors
    * silently spawn executor on first use
* tokio (from user feedback) requires its user to start one manually

* some crates allow to go from one runtime to the other
    * eg async-compat to use tokio with other runtimes


* "Libraries exposing async APIs should not depend on a specific executor or reactor, unless they need to spawn tasks or define their own async I/O or timer futures. Ideally, only binaries should be responsible for scheduling and running tasks."