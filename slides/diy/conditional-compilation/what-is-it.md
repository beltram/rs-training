## What is conditional compilation 

* Rust generate native application
* Dependent on hardware and OS. 
* It's up to include or not some part of source code in compilation depending on condition evaluation
* So evaluate before compiling (pre-compiler)
* Allows building smaller/faster/specialized binaries by removing code that is useless in target environment. A byte code application would have all code for all target and would evaluate target condition at runtime.
* Very useful for making app that fit in constraint of embedded computing.

[📒](https://doc.rust-lang.org/reference/conditional-compilation.html)