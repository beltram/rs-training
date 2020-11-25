## Raw pointer

* Raw pointer are pointer not managed/checked by rust compiler.
* Pointer return by non rust language like C.

So, when dereference a raw pointer, rust compiler should not make pointer normal handling.  
We have to use unsafe to be allowed to dereference a raw pointer.