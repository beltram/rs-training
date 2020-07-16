## for with index

* use 'enumerate()'
* destructure in '(index, value)'

```rust
let vowels = vec!["a", "e", "i", "o", "u", "y"];
for (index, vowel) in vowels.iter().enumerate() {
    println!("{} is the {}th vowel", vowel, index);
}
for (age, year) in (1991..=2020).enumerate() {
    println!("Beltram was {} in {}", age, year);
}
```

[📒](https://doc.rust-lang.org/1.17.0/book/loops.html#enumerate)