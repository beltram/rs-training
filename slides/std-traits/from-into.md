## [From](https://doc.rust-lang.org/std/convert/trait.From.html) & [Into](https://doc.rust-lang.org/std/convert/trait.Into.html) (aka mappers)

```rust
struct Person { firstname: String }
struct Developer { nickname: String }

// this will also generate 'impl Into<Developer> for Person'
impl From<Person> for Developer {
    fn from(input: Person) -> Self {
        Self { nickname: input.firstname }
    }
}

let trambel = Developer::from(Person { firstname: "beltram".to_string() });
let trambel: Developer = Person { firstname: "beltram".to_string() }.into();
//           ^^^ explicitly declared type to pick the right Into variant
```

* don't implement [Into](https://doc.rust-lang.org/std/convert/trait.Into.html) directly, prefer implementing [From](https://doc.rust-lang.org/std/convert/trait.From.html)