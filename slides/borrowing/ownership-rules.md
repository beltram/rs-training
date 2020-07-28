## Ownership

* at some point in time, a variable can only be owned by 1 block
* when a variable is moved, its original block loses ownership
* moving does not deep copy heap memory (!= C++ pass by value)
* when a block ends, all its variables still owned are dropped