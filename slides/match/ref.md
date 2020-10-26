## ref pattern

* by default, local bindings take ownership
* it can be changed to borrow using the 'ref' keyword (or 'ref mut')

```rust
struct Disease<'a> { symptoms: Vec<&'a str> }
let patient = Disease { symptoms: vec!["headaches", "fever"] };
match patient {
    ref p /*:&Disease*/ if p.symptoms.contains(&"headaches")
        && p.symptoms.contains(&"fever") => true,
    _ => false
};
// without 'ref', 'p' would have taken ownership of 'patient' 
println!("{:?}", patient.symptoms); // hence this would have failed
// because 'Vec' does not 'impl Copy'
```

* see [this example](https://play.rust-lang.org/?version=stable&mode=debug&edition=2018&gist=de0800a0575a90b07b711681d90e4391)
without 'ref' which does not compile

[📒](https://doc.rust-lang.org/reference/patterns.html)