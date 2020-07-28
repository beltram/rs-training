## Borrowing

* using ampersand &
* allows passing a reference (a pointer) from block A to block B
* block B "borrows" the variable from block A
* block A keeps ownership of the variable
* when a block B ends, the variable is not deallocated

```rust
fn block_B(s: &String) { println!("Borrowing {}", s) }

{ // block A
    let x = String::from("x");
    println!("Owning {}", x);
    block_B(&x);
    println!("Still owning {}", x);
}
```

[📒](https://doc.rust-lang.org/1.17.0/book/references-and-borrowing.html)