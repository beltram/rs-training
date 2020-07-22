## match guard

* By default, identifier patterns bind a variable to a copy of or move from the matched value 
* It can be changed to bind a reference using the `ref` keyword (or `ref mut` for a mutable reference)

```rust
#[derive(Debug)]
struct Disease<'a> { symptoms: Vec<&'a str> }
fn main() {
    let patient = Disease { symptoms: vec!["headaches", "fever"] };
    let _has_covid = match patient {
        ref p if p.symptoms.contains(&"headaches") 
                && p.symptoms.contains(&"fever") => true,
        _ => false
    };
// This works. But without the ref keyword we' get a value borrowed after move
// for "patient". The match expression would have taken ownership of the variable
  println!("{:?}", patient);
}
```

[📒](https://doc.rust-lang.org/reference/patterns.html)
[💻](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=d9fd5341b352a44704b1ff30bc4e7913)