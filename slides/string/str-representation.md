## &str

```rust
let a_string: String = String::from("Pascal");
assert_eq!(16, std::mem::size_of::<&str>());
let a_str: &str = &a_string;
let a_str_slice: &str = &a_string[..];
```

```bash
                                  pointer
                                /   length
                              /   / 
                            +–––+–––+
                      stack │ • │ 8 │ <- a_str: &str or a_str_slice: &str
                            +–│–+–––+
                              │
                              │
                              │
                            +–V–+–––+–––+–––+–––+–––+
                      heap  │ P │ a │ s │ c │ a │ l │
                            +–––+–––+–––+–––+–––+–––+
                            [––––––– length ––––––––]
```

[📒](https://doc.rust-lang.org/1.17.0/book/strings.html)