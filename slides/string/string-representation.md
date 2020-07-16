## String

```rust
let a_string: String = String::from("Pascal");
assert_eq!(24, std::mem::size_of_val(&a_string));
```

```bash
                                  pointer
                                /   capacity
                              /   /  length
                            /   /   /
                         +–––+–––+–––+
                   stack │ • │ 8 │ 6 │ <- a_string: String
                         +–│–+–––+–––+
                           │
                           │
                         [–│–––––––– capacity –––––––––––]
                         +–V–+–––+–––+–––+–––+–––+–––+–––+
                   heap  │ P │ a │ s │ c │ a │ l │   │   │
                         +–––+–––+–––+–––+–––+–––+–––+–––+
                         [––––––– length ––––––––]
```

[📒](https://doc.rust-lang.org/1.17.0/book/strings.html)