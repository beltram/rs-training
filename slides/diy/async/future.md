## Async bases - futures crate
* futures crate contains:
    * traits and functions to do async
    * has an executor, but no reactor (so no timer or async IOs)
    * might be included in std at some point
    * Futures need to be polled to completion. This is the job of an executor. Some futures additionally need to wait for events from the kernel to know when there might be data ready to read from a file, or somesuch. A reactor handles this
    * is used by smol and async-std