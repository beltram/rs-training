## Async runtimes
* async-std and smol:
    * use the same reactor/executors
    * silently spawn executor on first use
* tokio (from user feedback) requires its user to start one manually

* some crates allow to go from one runtime to the other
    * eg async-compat to use tokio with other runtimes

* "Libraries exposing async APIs should not depend on a specific executor or reactor, unless they need to spawn tasks or define their own async I/O or timer futures. Ideally, only binaries should be responsible for scheduling and running tasks."