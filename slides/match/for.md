## for loop

* fn foo(PATTERN: TYPE) {}
* for loops take only [irrefutable](https://doc.rust-lang.org/book/ch18-02-refutability.html) patterns

```rust
fn main() {
    let v = vec!['a', 'b', 'c'];

    // The value following the for keyword is a pattern
    // So you can do everything possible with a pattern, like destructuring
    for (index, value) in v.iter().enumerate() {
        println!("{} is at index {}", value, index);
    }
    
}
```

[📒](https://doc.rust-lang.org/book/ch18-01-all-the-places-for-patterns.html#for-loops)
[💻](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=21cbe71d5967ca3787fd0acb46017e99)