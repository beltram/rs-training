## String

```rust
let a_string: String = String::from("Pascal");
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
                         [–│–––––––– capacity –––––––––––]
                           │
                         +–V–+–––+–––+–––+–––+–––+–––+–––+
                   heap  │ P │ a │ s │ c │ a │ l │   │   │
                         +–––+–––+–––+–––+–––+–––+–––+–––+
                         [––––––– length ––––––––]
```

[📒](https://doc.rust-lang.org/1.7.0/book/strings.html)