## From and Into (aka mappers)

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
//             ^^^ explicitly declared type to pick the right Into variant
```

* don't implement Into directly, prefer implementing From