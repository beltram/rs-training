## Loop

```rust
let temperature = 20;
let should_i_swimm = if temperature < 25 { false } else { true };
let mut i = 0;
loop {
    if i == 35 {
        println!("Let's go swimming");
        break;
    }
    i = i + 1;
};
for g in ["A", "B", "C"].iter() {
    println!("I got an {} at my exam !", g);
}
["A", "B", "C"].iter().for_each(|g| println!("I got an {} at my exam !", g));
```
[📒](https://doc.rust-lang.org/1.7.0/book/loops.html) | 
[💻](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=bccf5886d84e73992078612136f71303)
